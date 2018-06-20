---
title: Prise en main du modèle objet JavaScript Project Server 2013
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30dc3194-7480-4e7c-b731-4a171d652ee0
description: Dans Project Server 2013, le modèle objet JavaScript utilisable dans Project Online, développement mobile et dans les locaux. Cette rubrique fournit une brève présentation du modèle objet JavaScript et puis explique comment créer une page d’application qui Récupère et effectue une itération dans les projets à l’aide du modèle objet JavaScript.
ms.openlocfilehash: 94c882249474e22328031d55233cfba654dcff83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787800"
---
# <a name="getting-started-with-the-project-server-2013-javascript-object-model"></a>Prise en main du modèle objet JavaScript Project Server 2013

Dans Project Server 2013, le modèle objet JavaScript utilisable dans Project Online, développement mobile et dans les locaux. Cette rubrique fournit une brève présentation du modèle objet JavaScript et puis explique comment créer une page d’application qui Récupère et effectue une itération dans les projets à l’aide du modèle objet JavaScript.
  
## <a name="using-the-project-server-javascript-object-model"></a>Utilisation du modèle objet JavaScript Project Server
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

À l’aide du modèle objet JavaScript est idéal pour créer une application qui s’exécute côté client (par opposition au code client managé qui doit être exécuté à distance). Applications peuvent utiliser le modèle objet JavaScript pour récupérer ou modifier des objets en envoyant des appels asynchrones au serveur. Les applications qui utilisent le modèle objet JavaScript sont généralement déployées en tant que compléments SharePoint, les pages d’application et les composants WebPart personnalisés. Pour plus d’informations, voir « Types de composants SharePoint pouvant se trouver dans une application pour SharePoint » dans [héberger des sites Web, dans Ajouter des sites Web et composants SharePoint dans SharePoint 2013](http://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx).
  
Le modèle objet JavaScript implémente les principales fonctionnalités de Project Server 2013, mais le modèle objet JavaScript et le modèle objet serveur n’ont pas de parité univoque. Le point d’entrée pour le modèle objet JavaScript est l’objet **ProjectContext** , qui représente le contexte client pour Project Server 2013 et donne accès au contenu du serveur et fonctionnalités. Le modèle objet JavaScript pour Project Server 2013 est défini dans le fichier PS.js, qui se trouve dans le chemin d’accès par défaut `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` sur le serveur d’applications. Project Server 2013 installe également le PM. Fichier Debug.js au même emplacement. PM. Debug.js est une version unminified de PS.js qui fournit des informations IntelliSense. 
  
Le modèle objet JavaScript permet à l’authentification par formulaires et toutes les demandes sont authentifiés en tant que l’utilisateur actuel. Pour plus d’informations sur la sécurité et d’autres considérations pour la conception des applications personnalisées et de solutions, voir [authentification, autorisation et sécurité dans SharePoint 2013](http://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx), [des aspects importants de l’architecture SharePoint Add-in et du développement Paysage](http://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx)et [compléments SharePoint par rapport aux solutions SharePoint](http://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx).
  
> [!NOTE]
> Pour accéder aux données à partir d’un site SharePoint à distance, SharePoint 2013 fournit une bibliothèque inter-domaines qui vous permet d’émettre des appels d’inter-domaines côté client. Pour plus d’informations, voir [data Access SharePoint 2013 des compléments à l’aide de la bibliothèque inter-domaines](http://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx). 
  
Nombre de concepts et de processus pour l’utilisation du modèle objet JavaScript pour Project Server 2013 semblables à celles de modèles objet client associés. Pour plus d’informations sur le modèle d’objet client managé Project Server 2013, voir **Microsoft.ProjectServer.Client**. Pour plus d’informations sur le modèle d’objet SharePoint 2013JavaScript et le modèle objet client managé, voir [effectuer des opérations base à l’aide de code de bibliothèque JavaScript dans SharePoint 2013](http://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) et [complète opérations de base à l’aide du client SharePoint 2013 code de bibliothèque](http://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx).
  
## <a name="walkthrough-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>Procédure : Création d’une page d’application qui récupère et parcourt les projets
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

Apprenez à créer une page d’application qui affiche l’ID, le nom et la date de création de chaque projet publié dans un site.
  
### <a name="prerequisites-for-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>Conditions préalables à la création d’une page d’application qui récupère et parcourt les projets
<a name="pj15_GetStartedJSOM_Prereqs"> </a>

Pour développer la page d’application décrite dans cette rubrique, vous devez installer et configurer les produits suivants :
  
- SharePoint Server 2013
- Project Server 2013 avec au moins un projet publié
- Visual Studio 2012
- Outils de développement Office pour Visual Studio 2012
    
Vous devez également disposer des autorisations pour déployer l’extension vers SharePoint Server 2013 et récupérer les projets.
  
> [!NOTE]
> Ces instructions supposent que vous développez sur l’ordinateur qui exécute Project Server 2013. 
  
### <a name="creating-the-application-page-in-visual-studio-2012"></a>Création de la page d’application dans Visual Studio 2012
<a name="pj15_GetStartedJSOM_CreateVS"> </a>

Les étapes suivantes permettent de créer un projet SharePoint et une page d’application qui contient un tableau et un libellé. Le tableau affiche des informations sur les projets et le libellé affiche des messages d’erreur.
  
1. Sur l’ordinateur qui exécute Project Server 2013, exécutez Visual Studio 2012 en tant qu’administrateur.
    
2. Créez un projet SharePoint 2013 vide, comme suit :
    
    1. Dans la boîte de dialogue **Nouveau projet**, sélectionnez **.NET Framework 4.5** dans la liste déroulante située en haut de la boîte de dialogue. 
        
    2. Dans la liste des catégories de modèles, choisissez la catégorie **Office SharePoint** , puis choisissez le modèle de **Projet SharePoint 2013** . 
        
    3. Nommez le projet GetProjectsJSOM, puis cliquez sur le bouton **OK** . 
        
    4. Dans la boîte de dialogue **Assistant Personnalisation de SharePoint** , sélectionnez **déployer en tant qu’une solution de batterie de serveurs**, puis cliquez sur le bouton **OK** . 
    
3. Dans l’Explorateur de solutions, modifiez la valeur de la propriété **URL du Site** pour le projet **ProjectsJSOM** correspondre à l’URL de l’instance Project Web App (par exemple, `http://ServerName/PWA`).
    
4. Ouvrez le menu contextuel du projet **GetProjectsJSOM** , puis ajoutez un SharePoint dossier mappé « Dispositions ». 
    
5. Dans le dossier **dispositions** , ouvrez le menu contextuel pour le dossier **GetProjectsJSOM** , puis ajoutez une nouvelle page d’application SharePoint nommée ProjectsList.aspx.
    
   > [!NOTE]
   > Cet exemple n’utilise pas le fichier code-behind qui crée de Visual Studio 2012 pour la page d’application. 
  
6. Ouvrez le menu contextuel de la page **ProjectsList.aspx** et sélectionnez **définir comme élément de démarrage**.
    
7. Dans le balisage de la page **ProjectsList.aspx** , définissez une table et un espace réservé de message dans les balises **Asp : contenu** « Main », comme suit. 
    
    ```HTML
    <table width="100%" id="tblProjects">
        <tr id="headerRow">
            <th width="25%" align="left">Project name</th>
            <th width="25%" align="left">Created date</th>
            <th width="50%" align="left">Project ID</th>
        </tr>
    </table>
    <div id="divMessage">
        <br/>
        <span id="spanMessage" style="color: #FF0000;"></span>
    </div>
    ```

### <a name="retrieving-the-projects-collection"></a>Récupération de la collection de projets
<a name="pj15_GetStartedJSOM_RetrieveProjs"> </a>

Les étapes suivantes permettent de récupérer et d’initialiser la collection de projets.
  
1. Une fois les balises **div** , ajoutez une balise **SharePoint:ScriptLink** qui référence le fichier PS.js, comme suit. 
    
   ```HTML
    <SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
   ```

2. En dessous de la balise **SharePoint:ScriptLink** , ajoutez les balises **script** , comme suit. 
    
   ```HTML
    <script type="text/javascript">
        // Paste the remaining code snippets here, in the order that they are presented.
    </script>
   ```

3. Choisissez une variable globale pour stocker la collection de projets, comme suit.
    
   ```js
   var projects;
   ```

4. Appelez le **SP. SOD.executeOrDelayUntilScriptLoaded** pour s’assurer que le fichier PS.js est chargé avant l’exécution de votre code personnalisé. 
    
   ```js
   SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
   ```

5. Ajoutez une fonction qui se connecte au contexte actuel et qui récupère la collection de projets, comme suit.
    
   ```js
    function GetProjects() {
        // Initialize the current client context.
        var projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the
        // Name, CreatedDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, CreatedDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(onQuerySucceeded, onQueryFailed);
    }
   ```

   Certains objets clients que vous récupérez via le contexte contiennent pas de données jusqu'à ce qu’ils sont initialisés ; Autrement dit, les valeurs de propriété de l’objet ne peut pas accéder aux jusqu'à ce que l’objet est initialisé. En outre, pour les propriétés de type **ValueObject**, vous devez explicitement demander la propriété avant d’accéder à sa valeur. (Si vous essayez d’accéder à une propriété avant qu’il est initialisé, vous recevrez une exception **PropertyOrFieldNotInitializedException** .) 
    
   Pour initialiser un objet, vous appelez la méthode **load** (ou la méthode **loadQuery** ) et ensuite la méthode **executeQueryAsync** . 
    
   - L’appel de la fonction **charger** ou la fonction **loadQuery** enregistre une demande que vous souhaitez exécuter sur le serveur. Vous passez un paramètre qui représente l’objet que vous souhaitez récupérer. Si vous travaillez avec une propriété **ValueObject** , puis vous demandez également la propriété dans le paramètre. 
    
   - Appeler la fonction **executeQueryAsync** et envoie la demande de requête asynchrone au serveur. Vous passez une fonction de rappel de réussite et une fonction de rappel échec à appeler lors de la réponse du serveur est reçue. 
    
   Pour réduire le trafic réseau, demander uniquement les propriétés que vous souhaitez utiliser lorsque vous appelez la fonction **charger** . En outre, si vous travaillez avec plusieurs objets, regrouper plusieurs appels à la fonction **de charge** avant d’appeler la fonction **executeQueryAsync** lorsque cela est possible. 
    
### <a name="iterating-through-the-projects-collection"></a>Parcourir la collection de projets
<a name="pj15_GetStartedJSOM_IterateProjs"> </a>

Les étapes suivantes permettent de parcourir la collection de projets (si l’appel au serveur aboutit) ou d’afficher un message d’erreur (si l’appel échoue).
  
1. Ajoutez une fonction de rappel de succès qui parcourt la collection de projets, comme suit.
    
   ```js
    function onQuerySucceeded(sender, args) {
        // Get the enumerator and iterate through the collection.
        var projectEnumerator = projects.getEnumerator();
        while (projectEnumerator.moveNext()) {
            var project = projectEnumerator.get_current();
            // Create the row for the project's information.
            var row = tblProjects.insertRow();
            // Insert cells for the Id, Name, and CreatedDate properties.
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_createdDate();
            row.insertCell().innerText = project.get_id();
        }
    }
   ```

2. Ajoutez une fonction de rappel d’échec qui affiche un message d’erreur, comme suit.
    
    ```js
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
    ```

3. Pour tester la page applications, dans la barre de menus, choisissez **débogage**, **Démarrer le débogage**. Si vous êtes invité à modifier le fichier web.config, cliquez sur **OK**.

<a name="pj15_GetStartedJSOM_CompleteExample"> </a>

## <a name="complete-code-example"></a>Exemple de code complet

Vous trouverez ci-dessous l’ensemble du code du fichier ProjectsList.aspx.
  
```js
<%@ Assembly Name="$SharePoint.Project.AssemblyFullName$" %>
<%@ Import Namespace="Microsoft.SharePoint.ApplicationPages" %>
<%@ Register Tagprefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="asp" Namespace="System.Web.UI" Assembly="System.Web.Extensions, Version=3.5.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35" %>
<%@ Import Namespace="Microsoft.SharePoint" %>
<%@ Assembly Name="Microsoft.Web.CommandUI, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="ProjectsList.aspx.cs" Inherits="GetProjectsJSOM.Layouts.GetProjectsJSOM.ProjectsList" DynamicMasterPageFile="~masterurl/default.master" %>
<asp:Content ID="PageHead" ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">
</asp:Content>
<asp:Content ID="Main" ContentPlaceHolderID="PlaceHolderMain" runat="server">
    <table width="100%" id="tblProjects">
    <tr id="headerRow">
        <th width="25%" align="left">Project name</th>
        <th width="25%" align="left">Created date</th>
        <th width="50%" align="left">Project ID</th>
    </tr>
</table>
<div id="divMessage">
    <br/>
    <span id="spanMessage" style="color: #FF0000;"></span>
</div>
<SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
<script type="text/javascript">
    // Declare a variable to store the published projects that exist
    // in the current context.
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
    // Get the projects collection.
    function GetProjects() {
        // Initialize the current client context.
        var projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the
        // Name, CreatedDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, CreatedDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(onQuerySucceeded, onQueryFailed);
    }
    function onQuerySucceeded(sender, args) {
        // Get the enumerator and iterate through the collection.
        var projectEnumerator = projects.getEnumerator();
        while (projectEnumerator.moveNext()) {
            var project = projectEnumerator.get_current();
            // Create the row for the project's information.
            var row = tblProjects.insertRow();
            // Insert cells for the Id, Name, and CreatedDate properties.
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_createdDate();
            row.insertCell().innerText = project.get_id();
        }
    }
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
</script>
</asp:Content>
<asp:Content ID="PageTitle" ContentPlaceHolderID="PlaceHolderPageTitle" runat="server">
Application Page
</asp:Content>
<asp:Content ID="PageTitleInTitleArea" ContentPlaceHolderID="PlaceHolderPageTitleInTitleArea" runat="server" >
My Application Page
</asp:Content>

```

<a name="pj15_GetStartedJSOM_AR"> </a>

## <a name="see-also"></a>Voir aussi

- [Créer, extraire, mettre à jour et supprimer des projets à l’aide du modèle objet Project Server JavaScript](create-retrieve-update-delete-projects-using-project-server-javascript.md)  
- [Modèle objet côté client (CSOM) pour Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Mise en route avec Project Server CSOM et .NET](getting-started-with-the-project-server-csom-and-net.md)
    

