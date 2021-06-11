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
ms.openlocfilehash: 659214a21dacf75b12f36cb6ad1e7f09c5af8800
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538367"
---
# <a name="initialization-and-clean-up-code-using-infopath-2003-object-model"></a>Code d'initialisation et de nettoyage à l'aide du modèle objet InfoPath 2003

Par défaut, le fichier FormCode.cs ou FormCode.vb créé pour un projet de modèle de formulaire compatible avec InfoPath 2003 contient tout le code source de la logique de programmation du formulaire. Le modèle du projet génère dans le fichier FormCode.cs ou FormCode.vb une classe similaire aux classes des exemples qui suivent, dans lesquels vous pouvez définir le code d'initialisation et de nettoyage, ainsi que les gestionnaires des événements du formulaire. Les fichiers FormCode.cs et FormCode.vb appliquent l'attribut de niveau assembly **System.ComponentModel.DescriptionAttribute** qui identifie la classe comme étant la seule classe dans laquelle sont implémentés les gestionnaires d'événements. L'attribut **InfoPathNamespace** (implémenté par le type [InfoPathNamespaceAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathNamespaceAttribute.aspx) ) est appliqué à la classe pour identifier les espaces de noms de la sélection du DOM XML utilisés dans la classe. Les espaces de noms référencés dans **InfoPathNamespace** sont gérés par le système de projet d'InfoPath. 
  
La classe FormCode elle-même fournit les méthodes  `_Startup` et  `_Shutdown` qui permettent d'effectuer des routines d'initialisation et de nettoyage pour tous les composants requis en plus de la fonctionnalité InfoPath standard lorsque le formulaire est ouvert. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Ne lancez pas d'appels à des membres du modèle objet InfoPath depuis les méthodes  `_Startup` et  `_Shutdown`. Il convient d'initialiser et d'appeler uniquement les membres des composants externes de ces méthodes. 
  
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

## <a name="the-_startup-method"></a>Méthode _Startup

Outre la fourniture d'un emplacement pour le code d'initialisation des composants supplémentaires, la méthode  `_Startup` initialise les variables  `thisXDocument` et  `thisApplication` qui peuvent être utilisées dans le code du formulaire pour accéder aux membres des classes [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) et [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) dans le modèle objet InfoPath. Le code nécessaire à l'initialisation de ces deux variables est généré automatiquement par le modèle de projet. 
  
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

Les exemples qui suivent présentent le gestionnaire d'événements d'un bouton qui utilise la variable  `thisXDocument` pour accéder à la méthode [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) du type [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) . 
  
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

Pour plus d’informations sur la création d’un handler d’événements, voir [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).
  
## <a name="the-_shutdown-method"></a>Méthode _ShutDown

La méthode  `_Shutdown` est la dernière méthode appelée à la fermeture du formulaire. Vous pouvez écrire dans cette méthode du code nécessaire au nettoyage ou à la finalisation des composants utilisés dans le formulaire. 
  
```cs
    public void _Shutdown()
    {
    }
```

```vb
    Public Sub _Shutdown()
    End    Sub
```

## <a name="initialization-and-clean-up-code-example"></a>Exemple de code d'initialisation et de nettoyage

L'exemple ci-dessous présente l'initialisation d'une connexion à une base de données Microsoft SQL Server dans la méthode  `_Startup` et la fermeture de cette connexion dans la méthode  `_Shutdown`. Pour que cet exemple fonctionne correctement, vous devez d'abord définir une référence à l'assembly System.Data de .NET Framework. Pour cela, cliquez sur **Ajouter une référence** dans le menu **Projet**, puis sélectionnez le composant System.Data.dll sous l'onglet **.NET**. Notez également que la directive  `using System.Data.SqlClient` (ou  `Imports System.Data.SqlClient)` a été ajoutée au début du fichier de code du formulaire pour réduire le nombre de frappes au clavier. 
  
> [!NOTE]
> [!REMARQUE] Les utilisateurs de formulaires InfoPath contenant un code de formulaire qui se connecte à une base de données SQL Server peuvent avoir besoin d'autorisations de sécurité en fonction des conditions de déploiement du formulaire et de la manière dont la stratégie de sécurité est définie. Pour plus d’informations sur la sécurité, voir À propos du modèle de sécurité pour les modèles de [formulaires](about-the-security-model-for-form-templates-with-code.md) avec code et configurer la sécurité Paramètres pour les [modèles](how-to-configure-security-settings-for-form-templates-with-code.md)de formulaire avec code . 
  
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

## <a name="see-also"></a>Voir aussi



[Ajouter un handler d’événements à l’aide du modèle objet InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

