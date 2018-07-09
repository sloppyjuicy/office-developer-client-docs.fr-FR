---
title: Code d'initialisation et de nettoyage à l'aide du modèle objet InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, clean-up code,InfoPath 2003-compatible form templates, initialization code
localization_priority: Normal
ms.assetid: 8d19e8fa-4e5c-40bb-ae89-7a552cc7914d
description: Par défaut, le fichier FormCode.cs ou FormCode.vb créé pour un projet de modèle de formulaire compatible avec InfoPath 2003 contient tout le code source de la logique de programmation du formulaire. Le modèle du projet génère dans le fichier FormCode.cs ou FormCode.vb une classe similaire aux classes des exemples qui suivent, dans lesquels vous pouvez définir le code d'initialisation et de nettoyage, ainsi que les gestionnaires des événements du formulaire. Les fichiers FormCode.cs et FormCode.vb appliquent l'attribut de niveau assembly System.ComponentModel.DescriptionAttribute qui identifie la classe comme étant la seule classe dans laquelle sont implémentés les gestionnaires d'événements. L'attribut InfoPathNamespace (implémenté par le type InfoPathNamespaceAttribute ) est appliqué à la classe pour identifier les espaces de noms de la sélection du DOM XML utilisés dans la classe. Les espaces de noms référencés dans InfoPathNamespace sont gérés par le système de projet d'InfoPath.
ms.openlocfilehash: 7111a8525b092998e21d4c267b5884f50fdb9777
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782381"
---
# <a name="initialization-and-clean-up-code-using-infopath-2003-object-model"></a><span data-ttu-id="d3d10-108">Code d'initialisation et de nettoyage à l'aide du modèle objet InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="d3d10-108">Initialization and Clean-up Code Using InfoPath 2003 Object Model</span></span>

<span data-ttu-id="d3d10-p102">Par défaut, le fichier FormCode.cs ou FormCode.vb créé pour un projet de modèle de formulaire compatible avec InfoPath 2003 contient tout le code source de la logique de programmation du formulaire. Le modèle du projet génère dans le fichier FormCode.cs ou FormCode.vb une classe similaire aux classes des exemples qui suivent, dans lesquels vous pouvez définir le code d'initialisation et de nettoyage, ainsi que les gestionnaires des événements du formulaire. Les fichiers FormCode.cs et FormCode.vb appliquent l'attribut de niveau assembly **System.ComponentModel.DescriptionAttribute** qui identifie la classe comme étant la seule classe dans laquelle sont implémentés les gestionnaires d'événements. L'attribut **InfoPathNamespace** (implémenté par le type [InfoPathNamespaceAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathNamespaceAttribute.aspx) ) est appliqué à la classe pour identifier les espaces de noms de la sélection du DOM XML utilisés dans la classe. Les espaces de noms référencés dans **InfoPathNamespace** sont gérés par le système de projet d'InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d3d10-p102">By default, the FormCode.cs or FormCode.vb file that is created for a form template project that is compatible with InfoPath 2003 contains all the source code for the programming logic of the form. The template for the project generates a class in the FormCode.cs or FormCode.vb file much like the classes in the following examples where you can define initialization and clean-up code, as well as handlers for form events. The FormCode.cs and FormCode.vb files apply an assembly-level **System.ComponentModel.DescriptionAttribute** attribute, which identifies the class as the only class where event handlers are implemented. The **InfoPathNamespace** attribute (which is implemented by the [InfoPathNamespaceAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathNamespaceAttribute.aspx) type) is applied to a class to identify the XML DOM selection namespaces used within the class. The namespaces referenced in the **InfoPathNamespace** are maintained by the InfoPath project system.</span></span> 
  
<span data-ttu-id="d3d10-114">La classe FormCode elle-même fournit les méthodes  `_Startup` et  `_Shutdown` qui permettent d'effectuer des routines d'initialisation et de nettoyage pour tous les composants requis en plus de la fonctionnalité InfoPath standard lorsque le formulaire est ouvert.</span><span class="sxs-lookup"><span data-stu-id="d3d10-114">The FormCode class itself provides  `_Startup` and  `_Shutdown` methods that are used to perform initialization and clean-up routines for any components that are required in addition to standard InfoPath functionality while the form is open.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="d3d10-p103">Ne lancez pas d'appels à des membres du modèle objet InfoPath depuis les méthodes  `_Startup` et  `_Shutdown`. Il convient d'initialiser et d'appeler uniquement les membres des composants externes de ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d3d10-p103">Do not call members of the InfoPath object model from within the  `_Startup` and  `_Shutdown` methods. You should initialize and call only members of external components in these methods.</span></span> 
  
```cs
using System;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
// Office integration attribute. Identifies the startup class for the form. Do not
// modify.
[assembly: System.ComponentModel.DescriptionAttribute(
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")]
namespace Template1
{
    // The namespace prefixes defined in this attribute must remain synchronized with
    // those in the form definition file (.xsf).
    [InfoPathNamespace(
        "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-29T22-27-27'")]
    public partial class FormCode
    {
        private XDocument thisXDocument;
        private Application thisApplication;
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            // You can add additional initialization code here.
        }
        public void _Shutdown()
        {
        }
    }
}
```

```vb
Imports System
Imports Microsoft.Office.Interop.InfoPath.SemiTrust
Imports Microsoft.VisualBasic
' Office integration attribute. Identifies the startup class for the form. Do not
' modify.
<Assembly: System.ComponentModel.DescriptionAttribute( _
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")>
Namespace Template1
    ' The namespace prefixes defined in this attribute must remain synchronized with
    ' those in the form definition file (.xsf).
    <InfoPathNamespace( _
        "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-29T22-36-40'")> _
    Public Class FormCode
        Private thisXDocument As XDocument
        Private thisApplication As Application
        Public Sub _Startup(app As Application, doc As XDocument)
            thisXDocument = doc
            thisApplication = app
            ' You can add additional initialization code here.
        End Sub
        Public Sub _Shutdown()
        End Sub
    End Class
End Namespace
```

## <a name="the-startup-method"></a><span data-ttu-id="d3d10-117">Méthode _Startup</span><span class="sxs-lookup"><span data-stu-id="d3d10-117">The _Startup Method</span></span>

<span data-ttu-id="d3d10-p104">Outre la fourniture d'un emplacement pour le code d'initialisation des composants supplémentaires, la méthode  `_Startup` initialise les variables  `thisXDocument` et  `thisApplication` qui peuvent être utilisées dans le code du formulaire pour accéder aux membres des classes [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) et [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) dans le modèle objet InfoPath. Le code nécessaire à l'initialisation de ces deux variables est généré automatiquement par le modèle de projet.</span><span class="sxs-lookup"><span data-stu-id="d3d10-p104">In addition to providing a place to write initialization code for additional components, the  `_Startup` method initializes the  `thisXDocument` and  `thisApplication` variables that can be used in your form code to access the members of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) and [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) classes in the InfoPath object model. The code necessary to initialize the two variables is generated automatically by the project template.</span></span> 
  
```cs
    private XDocument thisXDocument;
    private Application thisApplication;
    public void _Startup(Application app, XDocument doc)
    {
        thisXDocument = doc;
        thisApplication = app;
        // You can add additional initialization code here.
    }
```

```vb
    Private thisXDocument As XDocument
    Private thisApplication As Application
    Public Sub _Startup(app As Application, doc As XDocument)
        thisXDocument = doc
        thisApplication = app
        ' You can add additional initialization code here.
    End Sub

```

<span data-ttu-id="d3d10-120">Les exemples qui suivent présentent le gestionnaire d'événements d'un bouton qui utilise la variable  `thisXDocument` pour accéder à la méthode [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) du type [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d3d10-120">The following examples show a simple event handler for a button that uses the  `thisXDocument` variable to access the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) type.</span></span> 
  
```cs
[InfoPathEventHandler(MatchPath="CTRL1_5", EventType=InfoPathEventType.OnClick)]
public void CTRL1_5_OnClick(DocActionEvent e)
{
    // Write your code here.
    thisXDocument.UI.Alert("Hello!");
}
```

```vb
<InfoPathEventHandler(MatchPath:="CTRL1_5", EventType:=InfoPathEventType.OnClick)> _
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
    ' Write your code here.
    thisXDocument.UI.Alert("Hello!")
End Sub
```

<span data-ttu-id="d3d10-121">Pour plus d’informations sur la création d’un gestionnaire d’événements, voir [Ajouter un gestionnaire d’événement à l’aide du modèle objet InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="d3d10-121">For information on how to create an event handler, see [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span></span>
  
## <a name="the-shutdown-method"></a><span data-ttu-id="d3d10-122">Méthode _ShutDown</span><span class="sxs-lookup"><span data-stu-id="d3d10-122">The _ShutDown Method</span></span>

<span data-ttu-id="d3d10-p105">La méthode  `_Shutdown` est la dernière méthode appelée à la fermeture du formulaire. Vous pouvez écrire dans cette méthode du code nécessaire au nettoyage ou à la finalisation des composants utilisés dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="d3d10-p105">The  `_Shutdown` method is the last method called when a form is closed. You can write any code in this method that is needed to clean up or finalize components used in the form.</span></span> 
  
```cs
    public void _Shutdown()
    {
    }
```

```vb
    Public Sub _Shutdown()
    End    Sub
```

## <a name="initialization-and-clean-up-code-example"></a><span data-ttu-id="d3d10-125">Exemple de code d'initialisation et de nettoyage</span><span class="sxs-lookup"><span data-stu-id="d3d10-125">Initialization and Clean-up Code Example</span></span>

<span data-ttu-id="d3d10-p106">L'exemple ci-dessous présente l'initialisation d'une connexion à une base de données Microsoft SQL Server dans la méthode  `_Startup` et la fermeture de cette connexion dans la méthode  `_Shutdown`. Pour que cet exemple fonctionne correctement, vous devez d'abord définir une référence à l'assembly System.Data de .NET Framework. Pour cela, cliquez sur **Ajouter une référence** dans le menu **Projet**, puis sélectionnez le composant System.Data.dll sous l'onglet **.NET**. Notez également que la directive  `using System.Data.SqlClient` (ou  `Imports System.Data.SqlClient)` a été ajoutée au début du fichier de code du formulaire pour réduire le nombre de frappes au clavier.</span><span class="sxs-lookup"><span data-stu-id="d3d10-p106">The following example shows how to initialize a connection to a Microsoft SQL Server database in the  `_Startup` method and close the connection in the  `_Shutdown` method. In order for this example to work correctly, you must first set a reference to the System.Data assembly of the .NET Framework by clicking **Add Reference** on the **Project** menu, and then selecting the System.Data.dll component on the **.NET** tab. Also note that the  `using System.Data.SqlClient` (or  `Imports System.Data.SqlClient)` directive was added at the top of the form code file to reduce keystrokes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d3d10-128">Les utilisateurs de formulaires InfoPath contenant un code de formulaire qui se connecte à une base de données SQL Server peuvent avoir besoin d'autorisations de sécurité en fonction des conditions de déploiement du formulaire et de la manière dont la stratégie de sécurité est définie.</span><span class="sxs-lookup"><span data-stu-id="d3d10-128">Users of an InfoPath form that contains form code that connects to a SQL Server database may require security permissions depending on how the form is deployed and security policy is defined.</span></span> <span data-ttu-id="d3d10-129">Pour plus d’informations sur la sécurité, voir [Modèle de sécurité pour les modèles de formulaires avec Code](about-the-security-model-for-form-templates-with-code.md) et [Configurer les paramètres de sécurité pour les modèles de formulaire avec du Code](how-to-configure-security-settings-for-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="d3d10-129">For more information on security see [About the Security Model for Form Templates with Code](about-the-security-model-for-form-templates-with-code.md) and [Configure Security Settings for Form Templates with Code](how-to-configure-security-settings-for-form-templates-with-code.md).</span></span> 
  
```cs
using System;
using System.Data.SqlClient;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
// Office integration attribute. Identifies the startup class for the form. Do not
// modify.
[assembly: System.ComponentModel.DescriptionAttribute(
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")]
namespace Template1
{
    // The namespace prefixes defined in this attribute must remain synchronized with
    // those in the form definition file (.xsf).
    [InfoPathNamespace(
        "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-05T20-56-13'")]
    public partial class Template1
    {
        private XDocument    thisXDocument;
        private Application    thisApplication;
        private SqlConnection sqlConnect;
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            // Initialize variable for SQL Server connection.
            sqlConnect= new SqlConnection("server=localhost;Trusted_Connection=yes;database=Northwind");
        }
        public void _Shutdown()
        {
            // Close SQL Server connection at shut down.
            sqlConnect.Close();
        }
    }
}
```

```vb
Imports System
Imports System.Data.SqlClient
Imports Microsoft.Office.Interop.InfoPath.SemiTrust
Imports Microsoft.VisualBasic
' Office integration attribute. Identifies the startup class for the form. Do not
' modify.
<Assembly: System.ComponentModel.DescriptionAttribute( _
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")>
Namespace Template1
        ' The namespace prefixes defined in this attribute must remain synchronized with
        ' those in the form definition file (.xsf).
        <InfoPathNamespace( _
            "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-08T18-47-33'")>        _
        Public Class Template1
            Private thisXDocument As XDocument
            Private thisApplication As Application
            Private sqlConnect As SqlConnection
            Public Sub _Startup(app As Application, doc As XDocument)
                thisXDocument = doc
                thisApplication = app
                ' Initialize variable for SQL Server connection.
                sqlConnect = New SqlConnection _("server=localhost;Trusted_Connection=yes;database=Northwind")
            End Sub
        Public Sub _Shutdown()
            ' Close SQL Server connection.
            sqlConnect.Close()
        End Sub
    End Class
End Namespace
```

## <a name="see-also"></a><span data-ttu-id="d3d10-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3d10-130">See also</span></span>



[<span data-ttu-id="d3d10-131">Ajouter un gestionnaire d’événements à l’aide du modèle objet InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="d3d10-131">Add an Event Handler Using the InfoPath 2003 Object Model</span></span>](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

