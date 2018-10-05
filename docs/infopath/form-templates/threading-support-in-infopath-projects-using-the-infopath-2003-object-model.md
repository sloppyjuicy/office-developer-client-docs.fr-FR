---
title: Prise en charge du threading dans les projets InfoPath à l'aide du modèle de projet InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- multithreading [infopath 2007], infopath 2003-compatible form templates,threading [InfoPath 2007], support for projects using InfoPath 2003 object model,InfoPath 2003-compatible form templates, threading support
localization_priority: Normal
ms.assetid: f269d64d-4102-426d-be8e-d2742a993524
description: Les objets COM auxquels vous accédez via les assemblys d'interopérabilité Microsoft.Office.Interop.InfoPath.dll, Microsoft.Office.Interop.InfoPath.SemiTrust.dll et Microsoft.Office.Interop.InfoPath.Xml.dll installés par Microsoft InfoPath ne prennent pas en charge les appels sur plusieurs threads. Ceci inclut les interfaces pour les objets MSXML (Microsoft XML Core Services) incorporées dans l'espace de noms Microsoft.Office.Interop.InfoPath.SemiTrust (dont la plupart portent un nom commençant par IXMLDOM) et toutes les interfaces exposées par l'espace de noms Microsoft.Office.Interop.InfoPath.Xml, aucune de ces interfaces n'étant sécurisées pour l'utilisation de threads.
ms.openlocfilehash: 1be2bd0181c47097440af54f1aa804a4f17b30bf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395559"
---
# <a name="threading-support-in-infopath-projects-using-the-infopath-2003-object-model"></a>Prise en charge du threading dans les projets InfoPath à l'aide du modèle de projet InfoPath 2003

Les objets COM auxquels vous accédez via les assemblys d'interopérabilité Microsoft.Office.Interop.InfoPath.dll, Microsoft.Office.Interop.InfoPath.SemiTrust.dll et Microsoft.Office.Interop.InfoPath.Xml.dll installés par Microsoft InfoPath ne prennent pas en charge les appels sur plusieurs threads. Cela inclut les interfaces pour les objets de Microsoft XML Core Services (MSXML) qui sont inclus par l’espace de noms **Microsoft.Office.Interop.InfoPath.SemiTrust** (la plupart d'entre eux ont des noms qui portent le préfixe IXMLDOM) et toutes les interfaces exposées par l’espace de noms [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) , qui sont thread-safe. 
  
Tous les appels lancés vers ces objets COM doivent l'être sur un seul thread. Le code géré dans un projet InfoPath peut créer d'autres threads pour effectuer des tâches en arrière-plan, mais le code qui s'exécute sur des threads autres que le thread principal ne peut pas effectuer d'appels vers les modèles objets InfoPath.
  
Si votre projet InfoPath avec code géré utilise plusieurs threads, vous devez prêter attention au partage d'objets entre threads. Aucune référence au DOM XML ou référence aux objets InfoPath ne doit être partagée entre threads. 
  
## <a name="making-asynchronous-calls-to-the-infopath-object-model"></a>Appels asynchrones au modèle objet InfoPath

Pour les situations dans lesquelles il est nécessaire de lancer des appels vers un processus tel qu'un minuteur qui s'exécute dans un thread distinct, il est possible de remédier au fait que le modèle objet InfoPath n'accepte pas de tels appels. 
  
L'exemple suivant crée une instance **System.Timers.Timer** dans la méthode _Startup du formulaire et renvoie un appel asynchrone au minuteur. En outre, une instance de l’écran de la fenêtre (**System.Windows.Forms.Form**) invisible est créée. Lorsque la fonction de rappel écoulée du minuteur s'exécute une fois par seconde, elle appelle la fonction Win32 **PostMessage** pour publier un message dans la fenêtre invisible. Cette fenêtre invisible possède une fonction **WndProc** qui traite le message reçu de la fonction rappel du minuteur et met à jour le DOM XML du formulaire. Ce formulaire doit être installé comme formulaire avec autorisation totale pour pouvoir s'exécuter. Pour plus d’informations sur le débogage d’un modèle de formulaire entièrement fiable, voir [prévisualiser et déboguer les modèles de formulaires qui nécessitent une confiance totale](how-to-preview-and-debug-form-templates-that-require-full-trust.md). Pour plus d’informations sur le déploiement d’un modèle de formulaire entièrement fiable, voir [Déployer des modèles de formulaire InfoPath avec Code](how-to-deploy-infopath-form-templates-with-code.md).
  
```cs
using System;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
using System.Timers;
using System.Runtime.InteropServices;
// Office integration attribute. Identifies the startup class for the
// form. Do not modify.
[assembly: System.ComponentModel.DescriptionAttribute("InfoPathStartupClass, Version=1.0, Class=AsyncUpdate.AsyncUpdate")]
namespace AsyncUpdate
{
    public class User32
    {
        [DllImport("User32.dll")]
        public static extern Int32 PostMessage(
            IntPtr hWnd, int Msg, int wParam, int lParam);
        public User32()
        {    
        }
        ~User32()
        {
        }
    }
    public class MyWindow : System.Windows.Forms.Form
    {
        private XDocument thisXDocument;
        private AsyncUpdate thisProcess ;
        // Private message for internal class.
        public const int WM_MYNOTIFY = 0x400;
        public MyWindow(XDocument doc, AsyncUpdate process)
        {
            thisXDocument = doc;
            thisProcess  = process;
            this.Text = "MyWindow";
            // Force HWND to get created in Win32
            IntPtr hwnd = this.Handle; 
        }
        [System.Security.Permissions.PermissionSet(System.Security.Permissions.SecurityAction.Demand, Name="FullTrust")]
        protected override void WndProc(
            ref System.Windows.Forms.Message m) 
        {
            switch (m.Msg)
            {
            case WM_MYNOTIFY:
                IXMLDOMNode xml = thisXDocument.DOM.selectSingleNode(
                    "/my:myFields/my:field1");
                xml.text = thisProcess.counter.ToString();
                break;                
            }
            base.WndProc(ref m);
        }
    }
    // The namespace prefixes defined in this attribute must remain 
    // synchronized with those in the form definition file (.xsf).
    [InfoPathNamespace("xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2004-02-11T23-29-59'")]
    public class AsyncUpdate
    {
        private XDocument thisXDocument;
        private Application thisApplication;
        public int counter;
        private System.Timers.Timer myTimer;
        private MyWindow myWnd;
    
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            // init the counter
            counter = 0;
            // Start a timer on another thread
            myTimer = new System.Timers.Timer(1000);
            myTimer.Elapsed += new ElapsedEventHandler(
                myTimer_Elapsed);
            myTimer.Start();
            // create hidden window to receive notifications 
            // back on the main thread
            myWnd = new MyWindow(thisXDocument, this);
        }
        public void _Shutdown()
        {
            myWnd.Dispose();
            myTimer.Stop();
            myTimer.Dispose();
        }
        private void myTimer_Elapsed(object sender, ElapsedEventArgs e)
        {
            // This method is called on a second thread
            counter ++;
            // Post message back to main thread
            User32.PostMessage(
                myWnd.Handle, MyWindow.WM_MYNOTIFY, 0, 0);
        }
    }
}

```


