---
title: 'Procédure pas à pas : Créer un modèle de formulaire de base avec du code'
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- '[infopath 2007] de modèles de formulaire, création de code managé, géré de modèles de formulaires [InfoPath 2007], création de code, de modèles [InfoPath 2007], procédures pas à pas, InfoPath 2007, procédures pas à pas'
localization_priority: Normal
ms.assetid: 0f55c8be-8641-476a-b0c8-c88adb2ac2b9
description: Dans Microsoft InfoPath, vous pouvez écrire une logique métier dans Visual Basic ou Visual C# en l’ouverture d’un modèle de formulaire dans le Concepteur InfoPath, puis en utilisant une des commandes de l’interface utilisateur pour ajouter un gestionnaire d’événements, afin d’ouvre l’environnement de développement Visual Studio 2012 pour écriture de votre code.
ms.openlocfilehash: 8c98d71c26f8e56c532b2a4467218c366072b2ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782483"
---
# <a name="walkthrough-create-a-basic-form-template-with-code"></a>Procédure pas à pas : Créer un modèle de formulaire de base avec du code

Dans Microsoft InfoPath, vous pouvez écrire une logique métier dans Visual Basic ou Visual C# en l’ouverture d’un modèle de formulaire dans le Concepteur InfoPath, puis en utilisant une des commandes de l’interface utilisateur pour ajouter un gestionnaire d’événements, afin d’ouvre l’environnement de développement Visual Studio 2012 pour écriture de votre code. Par défaut, les projets de modèle de formulaire créé à l’aide de Visual Studio 2012 travail par rapport au modèle objet de code managé fourni par l’espace de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) . 
  
Cette procédure pas à pas vous montre tout d’abord comment créer une application Hello World simple à l’aide de c# ou Visual Basic dans l’environnement de développement Visual Studio 2012. La procédure pas à pas se termine par un exemple de code qui montre comment utiliser la propriété [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) de la classe [d’utilisateurs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) pour récupérer le nom de l’utilisateur actuel et remplir un contrôle de **Zone de texte** avec cette valeur. 
  
## <a name="prerequisites"></a>Conditions préalables

Pour pouvoir effectuer cette procédure à l’aide de l’environnement de développement Visual Studio 2012, vous aurez besoin :
  
- Microsoft InfoPath avec Visual Studio 2012 est installé.
    
## <a name="hello-world-in-visual-studio-tools-for-applications"></a>Créer l'application « Hello World » dans Visual Studio Tools for Applications

Dans la procédure suivante, vous allez découvrir comment écrire du code dans l’environnement de développement Visual Studio 2012 pour afficher une boîte de dialogue d’alerte simple en écrivant un gestionnaire d’événements pour l’événement [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) de la classe [ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) , qui est associée avec le contrôle **bouton** . 
  
### <a name="create-a-new-project-and-specify-the-programming-language"></a>Créer un projet et spécifier le langage de programmation

1. Démarrez le Concepteur InfoPath, puis double-cliquez sur le modèle de formulaire **vide (éditeur InfoPath)** . 
    
2. Pour spécifier le langage de programmation à utiliser, cliquez sur le **Bouton Office**et cliquez sur **Options de formulaire**, cliquez sur la **programmation** dans la liste **catégorie** , puis sélectionnez **Visual Basic** ou **Visual C#** dans le modèle de formulaire ** code de langue** liste déroulante. 
    
   > [!NOTE]
   > Les autres options linguistiques programmation dans la liste déroulante **langue du modèle de formulaire code** assurent la compatibilité avec les versions précédentes d’InfoPath. Les options **(InfoPath 2007 Compatible) c#** et **Visual Basic (InfoPath 2007 Compatible)** fonctionne avec les procédures décrites dans cette rubrique. Toutefois, pour utiliser les options **c# (compatible avec InfoPath 2003)** et **Visual Basic (compatible avec InfoPath 2003)** , voir [procédure pas à pas : création et débogage d’une base formulaire modèle à l’aide du modèle objet InfoPath 2003](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md). 
  
    Vous êtes maintenant prêt à ajouter un contrôle **bouton** et créer son gestionnaire d’événements. 
    
### <a name="add-a-button-control-and-event-handler"></a>Ajouter un contrôle Bouton et un gestionnaire d'événements

1. Dans le groupe **contrôles** , cliquez sur le contrôle **bouton** pour ajouter au formulaire. 
    
2. Double-cliquez sur le contrôle **bouton** , tapez Hello pour la propriété **Label** sous l’onglet **Propriétés** du ruban, puis cliquez sur **Code personnalisé**. Lorsque vous y êtes invité, enregistrez le formulaire et nommez-le HelloWorld.
    
   L’environnement **Visual Studio Tools for Applications** s’ouvre avec le curseur dans le gestionnaire pour l’événement [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) du **bouton** contrôle d’événements. 
    
   Vous pouvez maintenant ajouter du code de formulaire au gestionnaire d'événements du bouton.  
    
### <a name="add-hello-world-code-to-the-event-handler-and-preview-the-form"></a>Ajouter le code « Hello World » au gestionnaire d'événements et afficher un aperçu du formulaire

1. Dans le squelette du gestionnaire d'événements, tapez :
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   Le code de votre modèle de formulaire doit se présenter ainsi :
    
   ```cs
    using Microsoft.Office.InfoPath;
    using System;
    using System.Windows.Forms;
    using System.Xml;
    using System.Xml.XPath;
    namespace HelloWorld
    {
        public partial class FormCode
        {
            public void InternalStartup()
            {
            ((ButtonEvent)EventManager.ControlEvents["CTRL1_5"]).Clicked += new ClickedEventHandler(CTRL1_5_Clicked);
            }
            public void CTRL1_5_Clicked(object sender, ClickedEventArgs e)
            {
            MessageBox.Show("Hello World!");
            }
        }
    }
   ```

   ```vb
    Imports Microsoft.Office.InfoPath
    Imports System
    Imports System.Windows.Forms
    Imports System.Xml
    Imports System.Xml.XPath
    Namespace HelloWorld
        Public Class FormCode
            Private Sub InternalStartup(ByVal sender As Object, ByVal e As EventArgs) Handles Me.Startup
            AddHandler DirectCast(EventManager.ControlEvents("CTRL1_5"), ButtonEvent).Clicked, AddressOf CTRL1_5_Clicked
            End Sub
            Public Sub CTRL1_5_Clicked(ByVal sender As Object, ByVal e As ClickedEventArgs)
            MessageBox.Show("Hello World!")
            End Sub
        End Class
    End Namespace
   ```

2. Basculez dans la fenêtre Concepteur InfoPath.
    
3. Cliquez sur le bouton **Aperçu** sous l’onglet **accueil** . 
    
4. Cliquez sur le bouton Hello du formulaire. 
    
   Un message s'affiche avec le texte « Hello World! ».
    
   La procédure suivante illustre l'ajout de points d'arrêt pour le débogage dans le code de votre formulaire.
    
### <a name="debug-form-code"></a>Débogage de code de formulaire

1. Revenez à la fenêtre de Visual Studio 2012.
    
2. Cliquez sur la barre grise située à gauche de la ligne :
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   Un cercle rouge s'affiche et la ligne de code est mise en surbrillance pour indiquer que l'exécution marquera une pause à ce point d'arrêt dans votre code de formulaire.
    
3. Dans le menu **Débogage**, cliquez sur **Démarrer le débogage** ou appuyez sur F5. 
    
4. Dans la fenêtre **Aperçu** d’InfoPath, cliquez sur le bouton Hello du formulaire. 
    
5. L’éditeur de code Visual Studio 2012 reçoit le focus, et la ligne du point d’arrêt est mise en surbrillance.
    
6. Dans le menu **Débogage**, cliquez sur **Pas à pas principal** (ou appuyez sur Maj+F8 pour continuer pas à pas dans le code). 
    
7. Le gestionnaire d'événements est exécuté, et le message « Hello World! » s'affiche.  
    
8. Cliquez sur **OK** pour revenir à l’éditeur de code Visual Studio 2012, puis cliquez sur **Arrêter le débogage** dans le menu **débogage** (ou appuyez sur Ctrl + Alt + Attn). 
    
## <a name="getting-the-current-users-name"></a>Obtention du nom de l’utilisateur actuel

Dans l’exemple suivant, vous allez découvrir comment utiliser la propriété [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) de la classe [d’utilisateurs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) pour extraire le nom de l’utilisateur actuel et remplir la valeur d’un contrôle de **Zone de texte** à l’aide d’un gestionnaire d’événements pour l’événement de [chargement](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) . 
  
Remplissage du contrôle de **Zone de texte** s’effectue à l’aide d’une instance de la classe [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) pour écrire le nom de l’utilisateur actuel dans le nœud XML auquel le contrôle est lié à. 
  
La propriété [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) de la classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) est d’abord appelée pour récupérer une instance de la classe [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) qui représente le document XML sous-jacent du formulaire. L’objet [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) appelle ensuite la méthode [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) , qui crée l’objet **XPathNavigator** et le place sur le nœud racine de la source de données principale du formulaire. 
  
La méthode [SelectSingleNode](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.selectsinglenode%28v=vs.100%29.aspx) de la classe **XPathNavigator** est appelée pour sélectionner le champ employé dans la source de données du formulaire. Enfin, la méthode [SetValue](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.setvalue%28v=vs.100%29.aspx) est appelée pour définir la valeur du champ avec la propriété [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) . 
  
Pour plus d’informations sur l’utilisation de **System.Xml** dans les modèles de formulaires avec code managé, voir [utiliser les Classes XPathNavigator et XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
### <a name="add-a-loading-event-handler"></a>Ajouter un gestionnaire d'événements Chargement en cours (Loading) 

1. Ouvrez le modèle de formulaire HelloWorld que vous avez créé dans la procédure pas à pas précédente dans le Concepteur InfoPath.
    
2. Sous l’onglet **affichage** , sélectionnez **Afficher les champs**.
    
3. Cliquez avec le bouton droit sur le dossier **mesChamps** , puis cliquez sur **Ajouter**.
    
4. Dans **nom**, tapez employé, puis cliquez sur **OK**.
    
5. Faites glisser le champ employé sur l’affichage. 
    
6. Sous l’onglet **développeur** , cliquez sur **Événement chargement**.
    
   Cela crée un gestionnaire d’événements pour l’événement de [chargement](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) et placer le focus sur ce gestionnaire d’événements dans l’éditeur de code. 
    
7. Dans l'éditeur de code, tapez le code suivant :
    
   ```cs
    public void FormEvents_Loading(object sender, LoadingEventArgs e)
    {
        XPathNavigator dataSource;
        dataSource = this.MainDataSource.CreateNavigator();
        dataSource.SelectSingleNode(
            "/my:myFields/my:employee", NamespaceManager).SetValue(this.User.UserName);
    }
   ```
 
   ```vb
    Public Sub FormEvents_Loading(ByVal sender As Object, ByVal e As LoadingEventArgs)
        Dim dataSource As XPathNavigator
        dataSource = Me.MainDataSource.CreateNavigator
        dataSource.SelectSingleNode( _
            "/my:myFields/my:employee", NamespaceManager).SetValue(Me.User.UserName)
    End Sub
   ```

8. Basculer vers la fenêtre de création de formulaire InfoPath, puis cliquez sur le bouton **Aperçu** sous l’onglet **accueil** pour afficher un aperçu du formulaire. 
    
   Le champ employé doit être renseigné automatiquement votre nom d’utilisateur. 
    
## <a name="next-steps"></a>Étapes suivantes

- Pour plus d’informations sur l’utilisation des gestionnaires d’événements pour les autres contrôles et événements, voir [Ajouter un gestionnaire d’événements](how-to-add-an-event-handler.md).
    
- Pour plus d’informations sur l’aperçu et débogage de code dans les modèles de formulaires, voir [Aperçu et déboguer des modèles de formulaire InfoPath avec Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).
    
- Pour plus d’informations sur la façon de déployer un modèle de formulaire avec code managé, voir [Déployer des modèles de formulaire InfoPath avec Code](how-to-deploy-infopath-form-templates-with-code.md).
    
- Pour plus d’informations sur le modèle objet InfoPath et tâches de programmation courantes dans les modèles de formulaires avec code managé, voir [Présentation du modèle objet InfoPath et les tâches développeur courantes](understanding-the-infopath-object-model-and-common-developer-tasks.md)
    
## <a name="see-also"></a>Voir aussi

- [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)

