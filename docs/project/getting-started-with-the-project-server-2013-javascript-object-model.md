---
title: Prise en main du modèle objet JavaScript Project Server 2013
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 30dc3194-7480-4e7c-b731-4a171d652ee0
description: Dans Project Server 2013, le modèle objet JavaScript peut être utilisé dans Project Online développement local, mobile et mobile. Cette rubrique fournit une brève vue d’ensemble du modèle objet JavaScript, puis explique comment créer une page d’application qui récupère et itérera les projets à l’aide du modèle objet JavaScript.
ms.openlocfilehash: 6b568eccfe984c906dad30318cc512a03b44a2f2
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62465590"
---
# <a name="getting-started-with-the-project-server-2013-javascript-object-model"></a>Prise en main du modèle objet JavaScript Project Server 2013

Dans Project Server 2013, le modèle objet JavaScript peut être utilisé dans Project Online développement local, mobile et mobile. Cette rubrique fournit une brève vue d’ensemble du modèle objet JavaScript, puis explique comment créer une page d’application qui récupère et itérera les projets à l’aide du modèle objet JavaScript.
  
## <a name="using-the-project-server-javascript-object-model"></a>Utilisation du modèle objet JavaScript Project Server
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

L’utilisation du modèle objet JavaScript est un excellent moyen de créer une application qui s’exécute côté client (par opposition au code client géré qui doit s’exécuter à distance). Les applications peuvent utiliser le modèle objet JavaScript pour récupérer ou modifier des objets en envoyant des appels asynchrones au serveur. Les applications qui utilisent le modèle objet JavaScript sont généralement déployées en tant que SharePoint, les pages d’application et les composants WebPart. Pour plus d’informations, voir « Types de composants SharePoint qui peuvent se trouver dans une application pour SharePoint » dans les sites web hôtes, les sites web de SharePoint et les [composants de SharePoint dans SharePoint 2013](https://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx).
  
Le modèle objet JavaScript implémente la fonctionnalité principale de Project Server 2013, mais le modèle objet JavaScript et le modèle objet serveur n’ont pas de parité un-à-un. Le point d’entrée du modèle objet JavaScript est l’objet **ProjectContext**, qui représente le contexte client pour Project Server 2013 et fournit l’accès au contenu et aux fonctionnalités du serveur. Le modèle objet JavaScript pour Project Server 2013 est défini dans le fichier PS.js, `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` qui se trouve dans le chemin d’accès par défaut sur le serveur d’applications. Project Server 2013 installe également le fichier PS.Debug.js au même emplacement. Ce fichier est une version déminifiée de PS.js qui fournit des informations sur IntelliSense. 
  
Le modèle objet JavaScript permet l’authentification par formulaires et toutes les demandes sont authentifiées en tant qu’utilisateur actuel. Pour plus d’informations sur la sécurité et d’autres considérations pour la conception d’applications et de solutions personnalisées, voir l’authentification, l’autorisation et la sécurité dans [SharePoint 2013](https://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx), les aspects importants de [l’architecture](https://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx) et du développement des applications de SharePoint, ainsi que les solutions de SharePoint par rapport aux [solutions SharePoint](https://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx).
  
> [!NOTE]
> Pour accéder aux données à partir d’un site SharePoint à distance, SharePoint 2013 fournit une bibliothèque entre domaines qui vous permet d’effectuer des appels côté client entre domaines. Pour plus d’informations, [voir Access SharePoint 2013 à partir de modules complémentaires](https://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx) à l’aide de la bibliothèque entre domaines. 
  
De nombreux concepts et processus d’utilisation du modèle objet JavaScript pour Project Server 2013 ressemblent à ceux des modèles objet client associés. Pour plus d’informations sur Project modèle objet client géré Server 2013, voir **Microsoft.ProjectServer.Client**. Pour plus d’informations sur le modèle objet SharePoint 2013JavaScript et le modèle objet client géré, voir Effectuer des opérations de base à l’aide de code de bibliothèque [JavaScript dans SharePoint 2013](https://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) et Effectuer des opérations de base à l’aide de code de bibliothèque client [SharePoint 2013](https://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx).
  
## <a name="walkthrough-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>Procédure : Création d’une page d’application qui récupère et parcourt les projets
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

Apprenez à créer une page d’application qui affiche l’ID, le nom et la date de création de chaque projet publié dans un site.
  
### <a name="prerequisites-for-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>Conditions préalables à la création d’une page d’application qui récupère et parcourt les projets
<a name="pj15_GetStartedJSOM_Prereqs"> </a>

Pour développer la page d’application décrite dans cette rubrique, vous devez installer et configurer les produits suivants :
  
- SharePoint Server 2013
- Project Server 2013 avec au moins un projet publié
- Visual Studio 2012
- Outils de développement Office pour Visual Studio 2012
    
Vous devez également avoir les autorisations pour déployer l’extension sur SharePoint Server 2013 et récupérer des projets.
  
> [!NOTE]
> Ces instructions supposent que vous développez sur l’ordinateur qui exécute Project Server 2013. 
  
### <a name="creating-the-application-page-in-visual-studio-2012"></a>Création de la page d’application Visual Studio 2012
<a name="pj15_GetStartedJSOM_CreateVS"> </a>

Les étapes suivantes permettent de créer un projet SharePoint et une page d’application qui contient un tableau et un libellé. Le tableau affiche des informations sur les projets et le libellé affiche des messages d’erreur.
  
1. Sur l’ordinateur qui exécute Project Server 2013, exécutez Visual Studio 2012 en tant qu’administrateur.
    
2. Créez un projet SharePoint 2013 vide, comme suit :
    
    1. Dans la boîte de dialogue **Nouveau projet**, sélectionnez **.NET Framework 4.5** dans la liste déroulante située en haut de la boîte de dialogue. 
        
    2. Dans la liste des catégories de modèles, choisissez la catégorie **Office SharePoint**, puis sélectionnez le modèle **SharePoint 2013 Project**. 
        
    3. Nommez le projet GetProjectsJSOM, puis choisissez le **bouton OK** . 
        
    4. Dans la boîte de dialogue **Assistant Personnalisation de SharePoint**, choisissez **Déployer en tant que solution de batterie**, puis sélectionnez le bouton **OK**. 
    
3. Dans l’Explorateur de solutions, modifiez la valeur de la propriété **URL du site** pour le projet **ProjectsJSOM** afin qu’elle corresponde à l’URL de l’instance Project Web App (par exemple, `https://ServerName/PWA`).
    
4. Ouvrez le menu contextuel pour le projet **GetProjectsJSOM**, puis ajoutez un dossier mappé SharePoint nommé « Dispositions ». 
    
5. Dans le dossier **Layouts**, ouvrez le menu raccourci du dossier **GetProjectsJSOM**, puis ajoutez une nouvelle page d’application SharePoint nommée ProjectsList.aspx.
    
   > [!NOTE]
   > Cet exemple n’utilise pas le fichier code-behind que Visual Studio 2012 crée pour la page d’application. 
  
6. Ouvrez le menu contextuel de la page **ProjectsList.aspx** et choisissez **Définir comme élément de démarrage**.
    
7. Dans le balisage pour la page **ProjectsList.aspx**, définissez un tableau et un espace réservé de message dans les balises **asp:Content** « principales », comme suit. 
    
    ```HTML
    <table width="100%" id="tblProjects">
        <tr id="headerRow">
            <th width="25%" align="left">Project name</th>
            <th width="25%" align="left">Created date</th>
            <th width="50%" align="left">Project ID</th>
        </tr>
    </table>
    <div id="divMessage">
                <span id="spanMessage" style="color: #FF0000;"></span>
    </div>
    ```

### <a name="retrieving-the-projects-collection"></a>Récupération de la collection de projets
<a name="pj15_GetStartedJSOM_RetrieveProjs"> </a>

Les étapes suivantes permettent de récupérer et d’initialiser la collection de projets.
  
1. Après la fermeture de la balise **div**, ajoutez une balise **SharePoint:ScriptLink** qui fait référence au fichier PS.js, comme suit. 
    
   ```HTML
    <SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
   ```

2. Sous la balise **SharePoint:ScriptLink**, ajoutez des balises **script**, comme suit. 
    
   ```HTML
    <script type="text/javascript">
        // Paste the remaining code snippets here, in the order that they are presented.
    </script>
   ```

3. Choisissez une variable globale pour stocker la collection de projets, comme suit.
    
   ```js
   var projects;
   ```

4. Appelez la méthode **SP.SOD.executeOrDelayUntilScriptLoaded** pour vous assurer que le fichier PS.js est chargé avant l’exécution de votre code personnalisé. 
    
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

   Certains objets clients que vous récupérez via le contexte ne contiennent aucune donnée avant leur initialisation. Autrement dit, vous ne pouvez pas accéder aux valeurs de propriété de l’objet jusqu’à ce que l’objet soit initialisé. En outre, pour les propriétés de type **ValueObject**, vous devez demander la propriété de façon explicite avant d’accéder à sa valeur. (Si vous tentez d’accéder à une propriété avant son initialisation, vous recevez une exception **PropertyOrFieldNotInitializedException**.) 
    
   Pour initialiser un objet, appelez la méthode **load** (ou la méthode **loadQuery**), puis la méthode **executeQueryAsync**. 
    
   - L’appel de la fonction **load** ou **loadQuery** permet d’enregistrer une demande que vous souhaitez exécuter sur le serveur. Vous transmettez un paramètre qui représente l’objet que vous souhaitez récupérer. Si vous utilisez une propriété **ValueObject**, vous devez également demander la propriété dans le paramètre. 
    
   - L’appel de la fonction **executeQueryAsync** envoie la demande de requête au serveur de manière asynchrone. Vous transmettez une fonction de rappel de succès et d’échec à invoquer lorsque vous recevez la réponse du serveur. 
    
   Pour réduire le trafic réseau, demandez uniquement les propriétés que vous souhaitez utiliser lorsque vous appelez la fonction **load**. En outre, si vous utilisez plusieurs objets, si possible, regroupez plusieurs appels de la fonction **load** avant d’appeler la fonction **executeQueryAsync**. 
    
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

3. Pour tester la page d’application, dans la barre de menus, sélectionnez **Déboguer**, puis **Démarrer le débogage**. Si vous êtes invité à modifier le fichier web.config, cliquez sur **OK**.

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

- [Créer, récupérer, mettre à jour et supprimer des projets à l’aide du modèle objet JavaScript Project Server](create-retrieve-update-delete-projects-using-project-server-javascript.md)  
- [Modèle objet côté client (CSOM) pour Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Prise en main du modèle CSOM Project Server et de .NET](getting-started-with-the-project-server-csom-and-net.md)
    

