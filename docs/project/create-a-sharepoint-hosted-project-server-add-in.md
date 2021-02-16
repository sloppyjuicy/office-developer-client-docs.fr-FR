---
title: Créer un complément Project Server hébergé sur SharePoint
manager: lindalu
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: bb9c3c00-7121-41e1-9db3-75550d040ba8
description: Des trois types d’applications que vous pouvez créer pour Project Online (auto-hébergées, hébergées par un fournisseur et hébergées par SharePoint), l’application hébergée par SharePoint est la plus simple à créer et à déployer.
ms.openlocfilehash: 9b3b41eda40a8419ad72f11bb474acf7acaf81e9
ms.sourcegitcommit: 31b0a7373ff74fe1d6383c30bc67d7675b73d283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2020
ms.locfileid: "41773756"
---
# <a name="create-a-sharepoint-hosted-project-server-add-in"></a>Créer un complément Project Server hébergé sur SharePoint

Des trois types d’applications que vous pouvez créer pour Project Online (auto-hébergées, hébergées par un fournisseur et hébergées par SharePoint), l’application hébergée par SharePoint est la plus simple à créer et à déployer. Une application hébergée par SharePoint ne nécessite pas d’authentification OAuth et n’utilise pas Azure ou ne nécessite pas la maintenance d’un site local pour les ressources hébergées par un fournisseur. Le modèle **Application pour SharePoint 2013** dans Visual Studio est une infrastructure pratique pour le développement d’applications qui peuvent être publiées et vendues dans l’Office Store ou déployées dans un catalogue d’applications privé sur SharePoint. 
  
Dans Project, l’état est un processus dans lequel un membre d’équipe peut utiliser la page Tâches dans Project Web App pour envoyer l’état d’une tâche affectée, par exemple le nombre d’heures travaillées chaque jour d’une semaine passées à travailler sur la tâche. Le propriétaire de l’affectation (généralement, le responsable de projet) peut approuver ou rejeter l’état. Lorsque celui-ci est approuvé, Project recalcule la planification. L’application **QuickStatus** affiche les tâches affectées, où l’utilisateur peut rapidement mettre à jour le pourcentage achevé et envoyer l’état des affectations sélectionnées pour approbation. Bien que la page Tâches dans Project Web App offre beaucoup plus de fonctionnalités, l’application **QuickStatus** est un exemple qui fournit une interface simplifiée. 
  
**L’application QuickStatus** est un exemple pour les développeurs . il n’est pas destiné à être utilisé dans un environnement de production. L’objectif principal est d’afficher un exemple de développement d’applications pour Project Online, et non de créer une application d’état entièrement fonctionnelle. Pour une meilleure approche de l’état, voir la recommandation dans [les étapes suivantes.](#pj15_StatusingApp_NextSteps)
  
Pour obtenir des informations générales sur l’état, consultez [l’avancement des tâches.](https://support.office.com/article/Find-information-about-Project-Server-2013-8b08a414-15a7-4076-b2db-c90d0214ea7f?ui=en-US&rs=en-US&ad=US#BKMK_TaskProgress) Pour plus d’informations sur le développement de modules complémentaires pour SharePoint et Project Server, consultez La suite de [l’exemple.](https://msdn.microsoft.com/library/jj163230.aspx)

<a name="pj15_StatusingApp_Prerequisites"> </a>

## <a name="prerequisites-for-creating-an-app-for-project-server-2013"></a>Conditions préalables à la création d’une application pour Project Server 2013

Pour développer des applications relativement simples qui peuvent être déployées sur Project Online ou sur une installation sur site de Project Server 2013, vous pouvez utiliser les outils Napa, qui fournissent un environnement de développement en ligne. Pour les applications plus complexes, la modification du ruban Project Web App et la facilité de débogage pendant le développement, vous pouvez utiliser Visual Studio 2012 ou Visual Studio 2013. Par exemple, avec une installation locale, vous pouvez vérifier manuellement les modifications des DataTables brouillons dans la base de données Project Server. Cet article explique comment développer des applications avec Visual Studio.
  
Le développement d’applications Project Server avec Visual Studio nécessite les éléments suivants :
  
- Assurez-vous d’avoir installé les mises à jour Windows et les Service Packs les plus récents sur votre ordinateur de développement local. Le système d’exploitation peut être Windows 7, Windows 8, Windows Server 2008 ou Windows Server 2012.
    
- Vous devez avoir un ordinateur sur lequel SharePoint Server 2013 et Project Server 2013 sont installés, où l’ordinateur est configuré pour l’isolation et le chargement de version test des applications. Le chargement de version test permet à Visual Studio d’installer temporairement l’application pour le débogage. Vous pouvez utiliser une installation locale de SharePoint et Project Server. Pour plus d’informations, voir Configurer un environnement de développement [local pour les applications pour SharePoint.](https://msdn.microsoft.com/library/fp179923%28Office.15%29.aspx)
    
   > [!NOTE]
   > Pour une installation sur site, configurez un domaine d’application isolé avant  *de*  créer un catalogue d’applications d’entreprise. 
  
- L’ordinateur de développement peut être un ordinateur distant sur Visual Studio 2012. Assurez-vous que vous avez installé la version la plus récente ; voir la section *Outils* des [téléchargements d’applications pour Office et SharePoint.](https://msdn.microsoft.com/office/apps/fp123627.aspx)
    
- Vérifiez que l’instance Project Web App que vous utiliserez pour le développement et les tests est accessible dans le navigateur.
    
Pour plus d’informations sur l’utilisation des outils en ligne, voir Configurer un environnement pour le développement [d’applications pour SharePoint sur Office 365.](https://msdn.microsoft.com/library/fp161179.aspx) Pour une walkthrough de création d’une application simple pour Project Server qui utilise les outils en ligne, voir la série de blog EPMSource, Création de votre première [application Project Server](https://epmsource.com/2012/11/20/building-your-first-project-server-app-part-zerothe-introduction/).

<a name="pj15_StatusingApp_UsingVisualStudio"> </a>

## <a name="using-visual-studio-to-create-a-project-server-app"></a>Utilisation de Visual Studio pour créer une application Project Server

Outils de développement Office Visual Studio 2012 inclut un modèle pour les applications SharePoint qui peut être utilisé avec Project Server 2013. Lorsque vous créez une solution d’application, celle-ci inclut les fichiers suivants pour votre code personnalisé :
  
- **AppManifest.xml** comprend des paramètres pour le titre de l’application, l’étendue de demande d’autorisation et d’autres propriétés. La procédure 1 inclut les étapes pour définir les propriétés à l’aide du concepteur de manifeste. 
    
- **Default.aspx** dans le dossier Pages est la page principale de l’application. La procédure 2 décrit comment ajouter du contenu HTML5 à l’application **QuickStatus**. 
    
- **App.js** dans le dossier Scripts est le fichier principal pour le code JavaScript personnalisé. La procédure 3 explique le code JavaScript pour **l’application QuickStatus.** 
    
   Si vous ajoutez des contrôles commerciaux tels qu’une grille basée sur jQuery ou un s picker de date, vous pouvez ajouter des références à des fichiers JavaScript supplémentaires dans le fichier Default.aspx.
    
- **App.css** dans le dossier Contenu est le principal fichier pour les styles personnalisés CSS3. Les procédures 2 et 3 comprennent des informations sur les feuilles de style en cascade (CSS) pour l’application **QuickStatus**. Vous pouvez ajouter des références supplémentaires aux fichiers CSS dans le fichier Default.aspx. 
    
- **AppIcon.png** le dossier Images est l’icône 96 x 96 que l’application affiche dans l’Office Store ou le catalogue d’applications. 
    
Pour modifier le ruban Project Web App, vous pouvez ajouter une action personnalisée de ruban. La section [Exemple de code pour l’application QuickStatus](#pj15_StatusingApp_Example) contient le code complet pour les fichiers Default.aspx, App.js, App.css, Elements.xml et AppManifest.xml modifiés. 
  
### <a name="procedure-1-to-create-an-app-project-in-visual-studio"></a>Procédure 1. Pour créer un projet d’application dans Visual Studio

1. Exécutez Visual Studio 2012 en tant qu’administrateur, puis sélectionnez **Nouveau** projet sur la page de démarrage. 
    
2. Dans la boîte de dialogue **Nouveau projet**, développez les nœuds **Modèles**, **Visual C#** et **Office/SharePoint**, puis sélectionnez **Applications**. Utilisez l’option **.NET Framework 4.5** par défaut dans la liste déroulante de l’infrastructure cible en haut du volet central, puis sélectionnez **Application pour Office 2013** (voir la figure 1). 
    
3. Dans le **champ Nom,** tapez QuickStatus, accédez à l’emplacement où vous souhaitez enregistrer l’application, puis choisissez **OK.**
    
   **Figure 1. Création d’une application Project Server dans Visual Studio**

   ![Création d’une application Project Server dans Visual Studio](media/pj15_CreateStatusingApp_NewProject.gif "Création d’une application Project Server dans Visual Studio")
  
4. Dans la boîte de dialogue **Nouvelle application pour SharePoint**, renseignez les trois champs suivants : 
    
   - Dans la zone de texte supérieure, tapez le nom que vous souhaitez que l’application affiche dans Project Web App. Par exemple, saisissez Mise à jour de QuickStatus.
    
   - Pour le site à utiliser pour le débogage, tapez l’URL de l’instance de Project Web App. Par exemple,  `https://ServerName/ProjectServerName` tapez (en remplaçant  _ServerName_ et  _ProjectServerName_ par vos propres valeurs), puis choisissez **Valider**. Si tout se passe bien, Visual Studio affiche **Connexion réussie**. Si vous recevez un message d’erreur, assurez-vous que l’URL de Project Web App est correcte et que l’ordinateur Project Server est configuré pour l’isolation et le chargement de version test des applications. Pour plus d’informations, voir la section Conditions préalables à la création d’une [application pour Project Server 2013.](#pj15_StatusingApp_Prerequisites) 
    
   - Dans la liste déroulante **Comment souhaitez-vous héberger votre application pour SharePoint ?**, choisissez **Hébergement par SharePoint**.
    
   > [!CAUTION]
   > Si vous choisissez le type de projet par défaut **Hébergement par le fournisseur** par erreur, Visual Studio crée deux projets dans la solution : un projet **QuickStatus** et un projet **QuickStatusWeb**. Si deux projets apparaissent, supprimez cette solution et recommencez. 
  
5. Choisissez **OK** pour créer la solution **QuickStatus**, le projet **QuickStatus** et les fichiers par défaut. 
    
6. Ouvrez le concepteur de manifeste (par exemple, double-cliquez sur le fichier AppManifest.xml). Sur l’onglet **Général**, la zone de texte **Titre** doit afficher le nom de l’application saisi à l’étape 4. Choisissez l’onglet **Autorisations** afin d’ajouter les demandes d’autorisation suivantes pour l’application (voir figure 2) : 
    
   - Sur la première ligne de la liste **Demandes d’autorisation** dans la colonne **Étendue**, choisissez **État** dans la liste déroulante. Dans la colonne **Autorisation**, choisissez **SubmitStatus**.
    
   - Ajoutez une ligne là où l’option **Étendue** est définie sur **Plusieurs projets** et où **Autorisation** est définie sur **Lecture**.
    
   **Figure 2. Définition de l’étendue des autorisations pour une application d’état**

   ![Définition de l’étendue des autorisations pour une application d’état](media/pj15_CreateStatusingApp_PermissionScope.gif "Définition de l’étendue des autorisations pour une application d’état")
  
**L’application QuickStatus** permet à un utilisateur de Project Web App de lire les affectations de cet utilisateur à partir de plusieurs projets, de modifier le pourcentage d’affectation achevé et d’envoyer la mise à jour. Les autres étendues de demande d’autorisation figurant dans la liste déroulante de la figure 2 ne sont pas requises pour cette application. Les étendues de demande d’autorisation sont les autorisations demandées par l’application pour l’utilisateur. Si l’utilisateur n’a pas ces autorisations dans Project Web App, l’application ne s’exécute pas. Une application peut avoir plusieurs étendues de demande d’autorisation, y compris celles des autres autorisations SharePoint, mais doit avoir uniquement le minimum requis pour la fonctionnalité de l’application. Voici les étendues de demande d’autorisation qui sont liées à Project Server : 

- **Ressources d’entreprise**: autorisations du gestionnaire de ressources pour lire ou écrire des informations sur d’autres utilisateurs de Project Web App.
    
- **Plusieurs projets** : lecture ou écriture pour plusieurs projets, pour lesquels l’utilisateur dispose des autorisations demandées.
    
- **Project Server :** nécessite que l’utilisateur de l’application a des autorisations d’administrateur pour Project Web App.
    
- **Rapports**: lire le service **OData ProjectData** pour Project Web App (nécessite uniquement une autorisation de connexion pour Project Web App). 
    
- **Projet unique** : lecture ou écriture pour un projet pour lequel l’utilisateur dispose des autorisations demandées.
    
- **État** : envoi de mises à jour d’état des affectations, telles que les heures travaillées, le pourcentage achevé et les nouvelles affectations.
    
- **Flux de travail** : si l’utilisateur est autorisé à exécuter des flux de travail Project Server, l’application s’exécute ensuite avec des autorisations élevées pour le flux de travail.
    
Pour plus d’informations sur les étendues de demande d’autorisation pour Project Server 2013, voir la *section* Applications project dans Mises à jour pour les développeurs dans [Project 2013](updates-for-developers-in-project-2013.md) et autorisations d’application dans [SharePoint 2013.](https://msdn.microsoft.com/library/fp142383.aspx)


<a name="pj15_StatusingApp_HTML"> </a>

### <a name="creating-the-html-content-for-the-quickstatus-app"></a>Création de contenu HTML pour l’application QuickStatus

Avant de commencer à coder le contenu HTML, concevez l’interface utilisateur et l’expérience utilisateur pour l’application QuickStatus (la figure 3 montre un exemple de la page terminée). Une conception peut également inclure un plan des fonctions JavaScript qui interagissent avec le code HTML. Pour obtenir des informations générales, voir [conception de l’expérience UX pour les applications dans SharePoint 2013.](https://msdn.microsoft.com/library/fp179934.aspx)
  
**Figure 3. Conception de la page d’application QuickStatus**

![Conception de la page d’application QuickStatus](media/pj15_CreateStatusingApp_AfterRefresh.gif "Conception de la page d’application QuickStatus")
  
L’application affiche le nom complet en haut, qui est la valeur de l’élément **Title** dans AppManifest.Xml. 
  
Par défaut, la page utilise HTML5. Voici les éléments HTML standard pour les objets de l’interface utilisateur principale contenus par l’application **QuickStatus** dans le corps de la page : 
  
- Un élément **form** contient tous les autres éléments d’interface utilisateur. 
    
- Un élément **fieldset** crée un conteneur et la bordure du tableau des affectations. L’élément enfant **legend** fournit une étiquette pour le conteneur. 
    
- Un élément **table** inclut une légende et seulement un en-tête de tableau. Les fonctions JavaScript modifient la légende du tableau et ajoutent des lignes pour les affectations. 
    
   > [!NOTE]
   > Pour ajouter facilement une pagination et un tri, une application de production utilisera probablement un contrôle commercial de grille basée sur jQuery plutôt qu’un tableau. 
  
   Le tableau contient les colonnes pour le nom du projet, le nom de la tâche avec une case à cocher, le travail réel, le pourcentage achevé, le travail restant et la date de fin de l’affectation. Les fonctions JavaScript créent la case à cocher et le champ de saisie de texte pour le pourcentage achevé de chaque tâche.
    
- Un élément **input** pour une zone de texte définit le pourcentage achevé pour toutes les affectations sélectionnées. 
    
- Un élément **button** envoie les modifications d’état. 
    
- Un élément **button** actualise la page. 
    
- Un **élément bouton** quitte l’application et revient à la page Tâches dans Project Web App. 
    
Les éléments de bouton et de zone de texte inférieurs se trouvent dans les éléments **div**, afin que les CSS puissent gérer facilement la position et l’apparence des objets d’interface utilisateur. Une fonction JavaScript ajoute un paragraphe en bas de la page qui contient les résultats de la réussite ou de l’échec de la mise à jour d’état. 
  
### <a name="procedure-2-to-create-the-html-content"></a>Procédure 2. Pour créer du contenu HTML

1. Dans Visual Studio, ouvrez le fichier Default.aspx.
    
   Le fichier comprend deux **éléments asp:Content** : l’élément avec l’attribut est ajouté dans l’en-tête de page et l’élément avec l’attribut est placé dans l’élément de corps de `ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` `ContentPlaceHolderID="PlaceHolderMain"` page.  
    
2. Dans le contrôle de l’en-tête de page, ajoutez une référence au  `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">` fichier PS.js sur l’ordinateur Project Server. Pour le test et le débogage, vous pouvez utiliser PS.debug.js. 
    
   ```HTML
     <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
   ```

   L’infrastructure d’application utilise `/_layouts/15/` le répertoire virtuel pour le site SharePoint dans IIS. Le fichier physique est  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.debug.js` .
    
   > [!NOTE]
   > Avant de déployer l’application pour une utilisation en production, supprimez des  `.debug` références de script pour améliorer les performances. 
  
3. Dans le contrôle du corps de la page, supprimez l’élément div généré, puis ajoutez le code HTML pour les objets `<asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">` d’interface  utilisateur. L’élément **table** contient une ligne d’en-tête. La colonne **Nom de la tâche** inclut un contrôle d’entrée de case à cocher. Le texte pour l’élément **caption** est remplacé par le rappel **onGetUserNameSuccess** pour la fonction **getUserInfo** dans le fichier App.js. 
    
    ```HTML
    <form>
        <fieldset>
        <legend>Select assigned tasks</legend>
        <table id="assignmentsTable">
            <caption id="tableCaption">Replace caption</caption>
            <thead>
            <tr id="headerRow">
                <th>Project name</th>
                <th><input type="checkbox" id="headercheckbox" checked="checked" />Task name</th>
                <th>Actual work</th>
                <th>% complete</th>
                <th>Remaining work</th>
                <th>Due date</th>
            </tr>
            </thead>
        </table>
        </fieldset>
        <div id="inputPercentComplete" >
        Set percent complete for all selected assignments, or leave this
        <br /> field blank and set percent complete for individual assignments: 
        <input type="text" name="percentComplete" id="pctComplete" size="4"  maxlength="4" />
        </div>
        <div id="submitResult">
        <p><button id="btnSubmitUpdate" type="button" class="bottomButtons" ></button></p>
        <p id="message"></p>
        </div>
        <div id="refreshPage">
        <p><button id="btnRefresh" type="button" class="bottomButtons" >Refresh</button></p>
        </div>
        <div id="exitPage">
        <p><button id="btnExit" type="button" class="bottomButtons" >Exit</button></p>
        </div>
    </form>
    ```

4. Dans le fichier App.css, ajoutez le code CSS pour la position et l’apparence des éléments d’interface utilisateur. Pour obtenir le code CSS complet de l’application **QuickStatus**, consultez la section [Exemple de code pour l’application QuickStatus](#pj15_StatusingApp_Example). 
    
La procédure 3 ajoute les fonctions JavaScript pour lire les affectations et créer les lignes du tableau, ainsi que pour modifier et mettre à jour le pourcentage d’affectation achevé. Les étapes réelles sont plus itératives dans le développement d’une application, où vous pouvez également créer du code HTML, ajouter et tester des styles associés et des fonctions JavaScript, modifier ou ajouter du code HTML, puis répéter le processus.

<a name="pj15_StatusingApp_JavaScript"> </a>

### <a name="creating-the-javascript-functions-for-the-quickstatus-app"></a>Création des fonctions JavaScript pour l’application QuickStatus

Le modèle Visual Studio pour une application SharePoint inclut le fichier App.js contenant le code d’initialisation par défaut qui obtient le contexte client SharePoint et illustre les actions de base d’obtention et de définition de la page d’application. L’espace de noms JavaScript pour la bibliothèque de SP.js côté client SharePoint est **SP**. Étant donné qu’une application Project Server utilise la bibliothèque PS.js, l’application utilise l’espace de noms **PS** pour obtenir le contexte client et accéder au JSOM pour Project Server. 
  
Les fonctions JavaScript dans **l’application QuickStatus** sont les suivantes : 
  
- Le gestionnaire d’événements **ready** du document s’exécute lorsque le modèle objet de document (DOM) est instancié. Le gestionnaire d’événements **ready** effectue les quatre étapes suivantes : 
    
    1. Initialise la variable globale **projContext** avec le contexte client pour le JSOM Project Server et la variable globale **pwaWeb**. 
        
    2. Appelle la fonction **getUserInfo** pour initialiser la variable globale **projUser**. 
        
    3. Appelle la fonction **getAssignments**, qui obtient les données d’affectation spécifiées pour l’utilisateur. 
        
    4. Lie les gestionnaires d’événements Click à la case à cocher de l’en-tête de tableau, et aux cases à cocher de chaque ligne du tableau. Les gestionnaires d’événements Click gèrent l’attribut **checked** des cases à cocher lorsque l’utilisateur active ou désactive une case à cocher dans le tableau. 
    
- Si la fonction **getAssignments** réussit, elle appelle la fonction **onGetAssignmentsSuccess**. Cette fonction insère une ligne dans le tableau pour chaque affectation, initialise les contrôles HTML dans chaque ligne et initialise ensuite les propriétés du bouton inférieur. 
    
- Le **handler d’événement onClick** pour le bouton **Update** appelle la **fonction updateAssignments.** Cette fonction obtient la valeur de pourcentage achevé qui est appliquée à chaque affectation sélectionnée ; ou si la zone de texte pourcentage achevé est vide, la fonction obtient le pourcentage achevé de chaque affectation sélectionnée dans le tableau. La **fonction updateAssignments** enregistre et envoie ensuite les mises à jour d’état et écrit un message sur les résultats en bas de la page. 
    
### <a name="procedure-3-to-create-the-javascript-functions"></a>Procédure 3. Pour créer les fonctions JavaScript

1. Dans Visual Studio, ouvrez le fichier App.js, puis supprimez tout le contenu du fichier.
    
2. Ajoutez le gestionnaire d’événements **ready** des variables globales et du document. L’objet **document** est accessible à l’aide d’une fonction jQuery. 
    
   Le gestionnaire d’événements Click pour les cases à cocher d’en-tête de tableau définit l’état activé des cases à cocher de ligne. Si toutes les cases à cocher de ligne sont sélectionnées, ou toutes désactivées, le gestionnaire d’événements Click pour les cases à cocher de ligne définit l’état activé de la case à cocher d’en-tête. Les gestionnaires d’événements Click définissent également le message de résultats au bas de la page sur une chaîne vide.
    
   ```js
    var projContext;
    var pwaWeb;
    var projUser;
    // This code runs when the DOM is ready and creates a ProjectContext object.
    // The ProjectContext object is required to use the JSOM for Project Server.
    $(document).ready(function () {
        projContext = PS.ProjectContext.get_current();
        pwaWeb = projContext.get_web();
        getUserInfo();
        getAssignments();
        // Bind a click event handler to the table header check box, which sets the row check boxes
        // to the checked state of the header check box, and sets the results message to an empty string.
        $('#headercheckbox').live('click', function (event) {
            $('input:checkbox:not(#headercheckbox)').attr('checked', this.checked);
            $get("message").innerText = "";
        });
        // Bind a click event handler to the row check boxes. If any row check box is cleared, clear
        // the header check box. If all of the row check boxes are selected, select the header check box.
        $('input:checkbox:not(#headercheckbox)').live('click', function (event) {
            var isChecked = true;
            $('input:checkbox:not(#headercheckbox)').each(function () {
                if (this.checked == false) isChecked = false;
                $get("message").innerText = "";
            });
            $("#headercheckbox").attr('checked', isChecked);
        });
    });
   ```

3. Ajoutez la fonction **getUserInfo**, qui appelle **onGetUserNameSuccess** si la requête s’exécute correctement. La fonction **onGetUserNameSuccess** remplace le contenu du paragraphe **caption** par une légende de tableau qui inclut le nom d’utilisateur. 
    
   ```js
        // Get information about the current user.
        function getUserInfo() {
            projUser = pwaWeb.get_currentUser();
            projContext.load(projUser);
            projContext.executeQueryAsync(onGetUserNameSuccess,
                // Anonymous function to execute if getUserInfo fails.
                function (sender, args) {
                    alert('Failed to get user name. Error: ' + args.get_message());
            });
        } 
        // This function is executed if the getUserInfo call is successful.
        function onGetUserNameSuccess() {
            var prefaceInfo = 'Assignments for ' + projUser.get_title();
            $('#tableCaption').text(prefaceInfo);
        }
   ```

4. Ajoutez la fonction **getAssignments**, qui appelle **onGetAssignmentsSuccess** (voir l’étape 5) si la requête d’affectation a réussi. L’option **Include** limite la requête pour renvoyer uniquement les champs spécifiés. 
    
   ```js
    // Get the collection of assignments for the current user.
    function getAssignments() {
        assignments = PS.EnterpriseResource.getSelf(projContext).get_assignments();
        // Register the request that you want to run on the server. The optional "Include" parameter 
        // requests only the specified properties for each assignment in the collection.
        projContext.load(assignments,
            'Include(Project, Name, ActualWork, ActualWorkMilliseconds, PercentComplete, RemainingWork, Finish, Task)');
        // Run the request on the server.
        projContext.executeQueryAsync(onGetAssignmentsSuccess,
            // Anonymous function to execute if getAssignments fails.
            function (sender, args) {
                alert('Failed to get assignments. Error: ' + args.get_message());
            });
    }
   ```

5. Ajoutez **la fonction onGetAssignmentsSuccess,** qui ajoute une ligne pour chaque affectation au tableau. La variable **prevProjName** permet de déterminer si une ligne est pour un autre projet. Si c’est le cas, le nom du projet est affiché en gras . si ce n’est pas le cas, le nom du projet est une chaîne vide. 
    
   > [!NOTE]
   > Le JSOM n’inclut pas les **propriétés TimeSpan** que le CSOM inclut, telles que **ActualWorkTimeSpan**. En revanche, le JSOM utilise des propriétés concernant le nombre de millisecondes, telles que la propriété [PS.StatusAssignment.actualWorkMilliseconds](https://msdn.microsoft.com/library/736bce1e-f734-0efe-6c5f-e0e891ab00ef%28Office.15%29.aspx). La méthode pour obtenir cette propriété est **\_ obtenir actualWorkMilliseconds**, qui renvoie une valeur d’un nombre réel. > la **méthode get_actualWork** renvoie une chaîne telle que « 3h ». Vous pouvez utiliser n’importe quelle valeur dans l’application **QuickStatus**, mais affichez-la différemment. La requête d’affectations inclut les deux propriétés, pour que vous puissiez tester la valeur pendant le débogage. Si vous supprimez la variable **actualWork**, vous pouvez également supprimer la propriété **ActualWork** dans la requête d’affectations. 
  
   Enfin, la fonction **onGetAssignmentsSuccess** initialise le bouton **Mettre à jour** et le bouton **Actualiser** avec les gestionnaires d’événements Click. La valeur de texte du bouton **Mettre à jour** peut également être définie dans le code HTML. 
    
   ```js
        // Get the enumerator, iterate through the assignment collection, 
        // and add each assignment to the table.
        function onGetAssignmentsSuccess(sender, args) {
            if (assignments.get_count() > 0) {
                var assignmentsEnumerator = assignments.getEnumerator();
                var projName = "";
                var prevProjName = "3D2A8045-4920-4B31-B3E7-9D0C5195FC70"; // Any unique name.
                var taskNum = 0;
                var chkTask = "";
                var txtPctComplete = "";
                // Constants for creating input controls in the table.
                var INPUTCHK = '<input type="checkbox" class="chkTask" checked="checked" id="chk';
                var LBLCHK = '<label for="chk';
                var INPUTTXT = '<input type="text" size="4"  maxlength="4" class="txtPctComplete" id="txt';
                while (assignmentsEnumerator.moveNext()) {
                    var statusAssignment = assignmentsEnumerator.get_current();
                    projName = statusAssignment.get_project().get_name();
                    // Get an integer, such as 3600000.
                    var actualWorkMilliseconds = statusAssignment.get_actualWorkMilliseconds(); 
                    // Get a string, such as "1h". Not used here.
                    var actualWork = statusAssignment.get_actualWork();
                    if (projName === prevProjName) {
                        projName = "";
                    }
                    prevProjName = statusAssignment.get_project().get_name();
                    // Create a row for the assignment information.
                    var row = assignmentsTable.insertRow();
                    taskNum++;
                    // Create an HTML string with a check box and task name label, for example:
                    // <input type="checkbox" class="chkTask" checked="checked" id="chk1" /> <label for="chk1">Task 1</label>
                    chkTask = INPUTCHK + taskNum + '" /> ' + LBLCHK + taskNum + '">' 
                        + statusAssignment.get_name() + '</label>';
                    txtPctComplete = INPUTTXT + taskNum + '" />';
                    // Insert cells for the assignment properties.
                    row.insertCell().innerHTML = '<strong>' + projName + '</strong>';
                    row.insertCell().innerHTML = chkTask;
                    row.insertCell().innerText = actualWorkMilliseconds / 3600000 + 'h';
                    row.insertCell().innerHTML = txtPctComplete;
                    row.insertCell().innerText = statusAssignment.get_remainingWork();
                    row.insertCell().innerText = statusAssignment.get_finish();
                    // Initialize the percent complete cell.
                    $get("txt" + taskNum).innerText = statusAssignment.get_percentComplete() + '%'
                }
            }
            else {
                $('p#message').attr('style', 'color: #0f3fdb');     // Blue text.
                $get("message").innerText = projUser.get_title() + ' has no assignments'
            }
            // Initialize the button properties.
            $get("btnSubmitUpdate").onclick = function() { updateAssignments(); };
            $get("btnSubmitUpdate").innerText = 'Update';
            $get('btnRefresh').onclick = function () { window.location.reload(true); };
            $get('btnExit').onclick = function () { exitToPwa(); };
        }
   ```

6. Ajoutez le gestionnaire d’événements Click **updateAssignments** pour le bouton **Mettre à jour**. Lorsque l’utilisateur modifie la valeur de pourcentage achevé d’une tâche ou ajoute une valeur dans la zone de texte **percentComplete**, la valeur peut être saisie dans plusieurs formats tels que « 60 », « 60% » ou « 60 % ». La méthode **getNumericValue** renvoie la valeur numérique de la saisie de texte. 
    
   > [!NOTE]
   > Dans une application conçue pour une utilisation en production, les valeurs d’entrée pour les informations numériques doivent inclure une validation de champ et une vérification des erreurs supplémentaires. 
  
   L’exemple **updateAssignments** inclut une vérification des erreurs de base et affiche les informations dans le paragraphe **message** au bas de la page : vert si la requête de mise à jour a réussi et rouge s’il existe une erreur d’entrée ou en cas d’échec de la requête de mise à jour. 
    
   Avant d’utiliser la méthode **submitAllStatusUpdates**, l’application doit enregistrer les mises à jour sur le serveur à l’aide de la méthode **PS.StatusAssignmentCollection.update**. 
    
   ```js
        // Update all checked assignments. If the bottom percent complete field is blank,
        // use the value in the % complete field of each selected row in the table.
        function updateAssignments() {
            // Get percent complete from the bottom text box.
            var pctCompleteMain = getNumericValue($('#pctComplete').val()).trim();
            var pctComplete = pctCompleteMain;
            var assignmentsEnumerator = assignments.getEnumerator();
            var taskNum = 0;
            var taskRow = "";
            var indexPercent = "";
            var doSubmit = true;
            while (assignmentsEnumerator.moveNext()) {
                var pctCompleteRow = "";
                taskRow = "chk" + ++taskNum;
                if ($get(taskRow).checked) {
                    var statusAssignment = assignmentsEnumerator.get_current();
                    if (pctCompleteMain === "") {
                        // Get percent complete from the text box field in the table row.
                        pctCompleteRow = getNumericValue($('#txt' + taskNum).val());
                        pctComplete = pctCompleteRow;
                    }
                    // If both percent complete fields are empty, show an error.
                    if (pctCompleteMain === "" && pctCompleteRow === "") {
                        $('p#message').attr('style', 'color: #e11500');     // Red text.
                        $get("message").innerHTML =
                            '<b>Error:</b> Both <i>Percent complete</i> fields are empty, in row '
                            + taskNum
                            + ' and in the bottom textbox.<br/>One of those fields must have a valid percent.'
                            + '<p>Please refresh the page and try again.</p>';
                        doSubmit = false;
                        taskNum = 0;
                        break;
                    }
                    if (doSubmit) statusAssignment.set_percentComplete(pctComplete);
                }
            } 
            // Save and submit the assignment updates.
            if (doSubmit) {
                assignments.update();
                assignments.submitAllStatusUpdates();
                projContext.executeQueryAsync(function (source, args) {
                    $('p#message').attr('style', 'color: #0faa0d');     // Green text.
                    $get("message").innerText = 'Assignments have been updated.';
                }, function (source, args) {
                    $('p#message').attr('style', 'color: #e11500');     // Red text.
                    $get("message").innerText = 'Error updating assignments: ' + args.get_message();
                });
            }
        }
        // Get the numeric part for percent complete, from a string. For example, with "20 %", return "20".
        function getNumericValue(pctComplete) {
            pctComplete = pctComplete.trim();
            pctComplete = pctComplete.replace(/ /g, "");    // Remove interior spaces.
            indexPercent = pctComplete.indexOf('%', 0);
            if (indexPercent > -1) pctComplete = pctComplete.substring(0, indexPercent);
            return pctComplete;
        }
   ```

7. Ajoutez **la fonction exitToPwa,** qui utilise le paramètre de chaîne de requête **SPHostUrl** pour l’URL du site Project Web App hôte. Pour revenir à la page Tâches,  `"/Tasks.aspx"` appendez-la à l’URL. Par exemple, la variable **spHostUrl** serait définie sur  `https://ServerName/ProjectServerName/Tasks.aspx` .
    
   La fonction **getQueryStringParameter** divise l’URL de la page **QuickStatus** pour extraire et renvoyer le paramètre spécifié dans les options de l’URL. Voici un exemple de la valeur **document.URL** pour le document **QuickStatus** (tout sur une seule ligne) : 
    
   ```HTML
    https://app-ef98082fa37e3c.servername.officeapps.selfhost.corp.microsoft.com/pwa/
        QuickStatus/Pages/Default.aspx
        ?SPHostUrl=https%3A%2F%2Fsphvm%2D85178%2Fpwa
        &SPLanguage=en%2DUS
        &SPClientTag=1
        &SPProductNumber=15%2E0%2E4420%2E1022
        &SPAppWebUrl=https%3A%2F%2Fapp%2Def98082fa37e3c%2Eservername
            %2Eofficeapps%2Eselfhost%2Ecorp%2Emicrosoft%2Ecom%2Fpwa%2FQuickStatus
   ```

   Pour l’URL précédente, la **fonction getQueryStringParameter** renvoie la valeur de chaîne de requête **SPHostUrl,**  `https://ServerName/pwa` . 
    
   ```js
        // Exit the QuickStatus page and go back to the Tasks page in Project Web App.
        function exitToPwa() {
            // Get the SharePoint host URL, which is the top page of PWA, and add the Tasks page.
            var spHostUrl = decodeURIComponent(getQueryStringParameter('SPHostUrl'))
                            + "/Tasks.aspx";
            // Set the top window for the QuickStatus IFrame to the Tasks page.
            window.top.location.href = spHostUrl;
        }
        // Get a specified query string parameter from the {StandardTokens} URL option string.
        function getQueryStringParameter(urlParameterKey) {
            var docUrl = document.URL;
            var params = docUrl.split('?')[1].split('&');
            for (var i = 0; i < params.length; i++) {
                var theParam = params[i].split('=');
                if (theParam[0] == urlParameterKey)
                    return decodeURIComponent(theParam[1]);
            }
        }
   ```

Si vous publiez l’application **QuickStatus** à ce stade et que vous l’ajoutez à Project Web App, l’application peut être exécuté à partir de la page Contenu du site, mais elle n’est pas facilement accessible aux utilisateurs. Pour aider les utilisateurs à trouver et à exécuter l’application, vous pouvez ajouter un bouton au niveau du ruban sur la page Tâches. La procédure 4 explique comment ajouter une action personnalisée de ruban. 

<a name="pj15_StatusingApp_ribbon"> </a>

### <a name="adding-a-ribbon-custom-action"></a>Ajout d’une action personnalisée du ruban

Les onglets du ruban, les groupes et les contrôles de Project Web App sont spécifiés dans le fichier pwaribbon.xml, qui est installé dans le répertoire sur l’ordinateur exécutant  `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\PWARibbon\listtemplates` Project Server. Pour vous aider à concevoir des actions personnalisées pour le ruban Project Web App, le téléchargement du SDK Project 2013 inclut une copie de pwaribbon.xml. 
  
Project Web App utilise différentes définitions de ruban pour la page Tâches, selon que l’instance de Project Web App utilise le mode d’entrée unique qui permet aux utilisateurs d’entrer des valeurs pour l’état de la feuille de temps et de la tâche. Si vous avez des autorisations administratives pour Project Web App, pour déterminer le mode d’entrée, choisissez **Paramètres PWA** dans le menu des paramètres de liste déroulante dans le coin supérieur droit de la page. Sur la page Paramètres PWA, sélectionnez **Paramètres et valeurs par défaut de la feuille de temps**, puis observez la case à cocher **Mode d’entrée unique** en bas de la page. 
  
Lorsque le mode d’entrée unique est désactivé, le ruban sur la page Tâches est défini par la région Mon travail dans pwaribbon.xml : 
  
```XML
   <!-- REGION My Work Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.MyWork"
      . . .
```

Lorsque le mode d’entrée unique est activé, le ruban sur la page Tâches est défini par la région Mode lié dans pwaribbon.xml : 
  
```XML
   <!-- REGION Tied Mode Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.TiedMode"
      . . .
```

Bien que les groupes et les contrôles de chaque région se ressemblent, un contrôle du mode lié peut appeler une fonction différente de celle appelée par le même contrôle pour le mode non lié. La procédure 4 explique comment ajouter un contrôle de bouton pour l’application **QuickStatus** lorsque le mode d’entrée unique est désactivé (la case à cocher **Mode d’entrée unique** est désactivée). 
  
> [!NOTE]
> Pour obtenir des informations générales sur l’ajout d’actions personnalisées à un ruban ou à un menu dans une application SharePoint, voir Créer des actions personnalisées à déployer avec des [applications pour SharePoint.](https://msdn.microsoft.com/library/jj163954.aspx) 
  
### <a name="procedure-4-to-add-a-ribbon-custom-action-to-the-tasks-page"></a>Procédure 4. Pour ajouter une action personnalisée de ruban sur la page Tâches

1. Examinez le ruban de la page Tâches dans Project Web App. Sélectionnez l’onglet **TÂCHES** dans le ruban et planifiez sa modification. Il existe sept groupes, tels que **Envoyer**, **Tâches** et **Période**. Le groupe **Envoyer** a deux contrôles, un bouton **Enregistrer** et un menu déroulant **Envoyer l’état**. Vous pouvez ajouter un contrôle à un emplacement quelconque dans un groupe, ajouter un groupe avec un nouveau contrôle à un emplacement quelconque dans l’onglet **TÂCHES** ou ajouter un autre onglet de ruban avec des groupes et contrôles personnalisés. Dans cet exemple, nous ajoutons un troisième bouton au groupe **Envoyer**, où le bouton appelle l’URL de l’application **QuickStatus**. 
    
2. Dans le volet **Explorateur de solutions** dans Visual Studio, cliquez avec le bouton droit sur le projet **QuickStatus** et ajoutez un nouvel élément. Dans la boîte de dialogue **Ajouter un nouvel élément**, sélectionnez **Action personnalisée de ruban** (voir Figure 4). Par exemple, nommez l’action personnalisée RibbonQuickStatusAction, puis choisissez **Ajouter**.
    
   **Figure 4. Ajout d’une action personnalisée de ruban**

   ![Ajout d’une action personnalisée du ruban](media/pj15_CreateStatusingApp_AddRibbonCustomAction.gif "Ajout d’une action personnalisée du ruban")
  
3. Sur la première page de l’assistant **Créer une action personnalisée pour le Ruban**, maintenez l’option **Hôte web** sélectionnée, choisissez **Aucun** dans la liste déroulante pour l’étendue de l’action personnalisée, puis **Suivant** (voir figure 5). Les éléments des listes déroulantes sont pertinents pour SharePoint, et non pour Project Server. Nous remplacerons une grande partie du code XML généré pour l’action personnalisée afin qu’elle s’applique à Project Server. 
    
   **Figure 5. Définition des propriétés pour l’action personnalisée de ruban**

   ![Définition des propriétés pour l’action personnalisée du ruban](media/pj15_CreateStatusingApp_RibbonCustomAction2.gif "Définition des propriétés pour l’action personnalisée du ruban")
  
4. Sur la page suivante de l’assistant **Créer une action personnalisée pour le Ruban**, maintenez toutes les valeurs par défaut pour les paramètres, puis sélectionnez **Terminer** (voir figure 6). Visual Studio crée le dossier **RibbonQuickStatusAction** qui contient un fichier Elements.xml. 
    
   **Figure 6. Définition des paramètres pour un contrôle de bouton**

   ![Définition des paramètres pour un contrôle bouton](media/pj15_CreateStatusingApp_RibbonCustomAction3.gif "Définition des paramètres pour un contrôle bouton")
  
5. Modifiez le code généré par défaut dans le fichier Elements.xml pour l’action personnalisée de ruban. Voici le code XML par défaut :
    
   ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="http://schemas.microsoft.com/sharepoint/">
        <CustomAction Id="21ea3aaf-79e5-4aac-9479-8eef14b4d9df.RibbonQuickStatusAction"
                    Location="CommandUI.Ribbon"
                    Sequence="10001"
                    Title="Invoke &apos;RibbonQuickStatusAction&apos; action">
        <CommandUIExtension>
            <!-- 
            Update the UI definitions below with the controls and the command actions
            that you want to enable for the custom action.
            -->
            <CommandUIDefinitions>
            <CommandUIDefinition Location="Ribbon.ListItem.Actions.Controls._children">
                <Button Id="Ribbon.ListItem.Actions.RibbonQuickStatusActionButton"
                        Alt="Request RibbonQuickStatusAction"
                        Sequence="100"
                        Command="Invoke_RibbonQuickStatusActionButtonRequest"
                        LabelText="Request RibbonQuickStatusAction"
                        TemplateAlias="o1"
                        Image32by32="_layouts/15/images/placeholder32x32.png"
                        Image16by16="_layouts/15/images/placeholder16x16.png" />
            </CommandUIDefinition>
            </CommandUIDefinitions>
            <CommandUIHandlers>
            <CommandUIHandler Command="Invoke_RibbonQuickStatusActionButtonRequest"
                                CommandAction="~appWebUrl/Pages/Default.aspx"/>
            </CommandUIHandlers>
        </CommandUIExtension >
        </CustomAction>
    </Elements>
   ```

   1. Dans l’élément **CustomAction**, supprimez l’attribut **Sequence** et l’attribut **Title**. 
    
   2. Pour ajouter un  contrôle au groupe d’soumission, recherchez le premier groupe de la collection dans le fichier pwaribbon.xml, qui est l’élément qui `Ribbon.ContextualTabs.MyWork.Home.Groups` commence. `<Group Id="Ribbon.ContextualTabs.MyWork.Home.Page" Command="PageGroup" Sequence="10" Title="$Resources:pwafeatures,PAGE_PDP_CM_SUBMIT"` Pour ajouter un contrôle enfant au groupe **Envoyer**, le code suivant illustre le bon attribut **Location** de l’élément **CommandUIDefinition** dans le fichier Elements.xml : 
    
      ```XML
        <CommandUIDefinitions>
          <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
             . . .
          </CommandUIDefinition>
        </CommandUIDefinitions>
      ```

   3. Modifier les valeurs d’attribut de l’élément enfant **Button** comme suit : 
    
       ```XML
            <Button Id="Ribbon.ContextualTabs.MyWork.Home.Page.QuickStatus"
                    Alt="Quick Status app"
                    Sequence="30"
                    Command="Invoke_QuickStatus"
                    LabelText="Quick Status"
                    TemplateAlias="o1"
                    Image16by16="_layouts/15/1033/images/ps16x16.png" 
                    Image16by16Left="-80"
                    Image16by16Top="-144"
                    Image32by32="_layouts/15/1033/images/ps32x32.png" 
                    Image32by32Left="-32"
                    Image32by32Top="-288" 
                    ToolTipTitle="QuickStatus"
                    ToolTipDescription="Run the QuickStatus app" />
       ```

       - Pour faire du bouton le troisième contrôle du groupe, l’attribut **Sequence** peut être un nombre supérieur à la valeur du contrôle d’état d’envoi existant (qui est un élément `Sequence="20"`  **FlyoutAnchor** dans pwaribbon.xml). Par convention, les numéros de séquence des groupes et des contrôles sont , ce qui permet d’insérer des éléments à  `10, 20, 30, …` des positions intermédiaires.
    
       - L’attribut **Command** spécifie la commande à exécuter dans l’élément **CommandUIHandler** (voir l’étape suivante, 5.d). Vous pouvez simplifier le nom de commande pour aider le développeur suivant. Par  `Command="Invoke_QuickStatus"` exemple, est plus facile à lire que  `Command="Invoke_RibbonQuickStatusActionButtonRequest"` .
    
       - Les attributs d’image spécifient l’icône de 16 x 16 pixels et l’icône de 32 x 32 pixels pour le contrôle de bouton. Dans le fichier Elements.xml par défaut,  `Image32by32="_layouts/15/images/placeholder32x32.png"` spécifie un point orange. Vous pouvez extraire des icônes des fichiers de carte image (ps16x16.png et ps32x32.png) installés dans le répertoire sur l’ordinateur exécutant  `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\1033\IMAGES` Project Server. Par exemple, l’icône de 32 x 32 pixels se trouve dans la deuxième colonne d’icônes à partir de la gauche et la dixième ligne vers le bas à partir du haut de la carte d’image ps32x32.png (le haut de l’icône se trouve après la fin de la neuvième ligne ; 9 lignes x 32 pixels/ligne = 288 pixels). 
    
       - Pour afficher une info-bulle pour le contrôle de bouton, ajoutez l’attribut **ToolTipTitle** et l’attribut **ToolTipDescription**. 
    
    4. Modifiez les attributs de l’élément **CommandUIHandler**. Par exemple, assurez-vous que l’attribut **Command** correspond à la valeur d’attribut **Command** de l’élément **Button**. Pour **l’attribut CommandAction,** `~appWebUrl` est un espace réservé pour l’URL de la page web **QuickStatus.** Lorsque le bouton du ruban appelle l’application **QuickStatus**, le jeton **{StandardTokens}** est remplacé par les options d’URL qui incluent **SPHostUrl**, **SPLanguage**, **SPClientTag**, **SPProductNumber** et **SPAppWebUrl**.
    
        ```XML
            <CommandUIHandlers>
                <CommandUIHandler Command="Invoke_QuickStatus"
                                  CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
            </CommandUIHandlers>
        ```

6. Dans l’**Explorateur de solutions**, ouvrez le concepteur **Feature1.feature**, puis déplacez l’élément **RibbonQuickStatusAction** du volet **Éléments dans la solution** vers le volet **Éléments dans la fonctionnalité**. Si vous ouvrez le concepteur **Package.package**, l’élément **RibbonQuickStatusAction** sera dans le volet **Éléments dans le package**. 
    
Lorsque vous développez l’application et ajoutez un bouton de ruban, vous testez normalement l’application et définissez des points d’arrêt dans le code JavaScript pour le débogage. Lorsque vous appuyez sur **F5** pour démarrer le débogage, Visual Studio compile l’application, la déploie sur le site spécifié dans la propriété **URL du site** du projet **QuickStatus** et affiche une page qui vous demande si vous faites confiance à l’application. Lorsque vous continuez, puis quittez **l’application QuickStatus,** elle revient à la page Tâches dans Project Web App. 

> [!NOTE]
> La figure 7 montre que le bouton **État rapide** sur l’onglet **TÂCHES** du ruban est désactivé. Après plusieurs déploiements de débogage avec Visual Studio, des contrôles de ruban personnalisé peuvent être bloqués lorsque vous continuez à déboguer ou déployer l’application publiée sur le même serveur de test. Pour activer le bouton, supprimez l’élément **RibbonQuickStatusAction** dans Visual Studio et créez une action de ruban avec un ID et un nom différents. Si cela ne résout pas le problème, essayez de supprimer l’application de l’instance de test Project Web App, puis recréez l’application avec un autre ID d’application. 
  
**Figure 7. Affichage de l’info-bulle du bouton État rapide désactivé**

![Affichage de l’info-bulle du bouton désactivé](media/pj15_CreateStatusingApp_ButtonToolTipDisabled.gif "Affichage de l’info-bulle du bouton désactivé")
  
La procédure 5 montre comment déployer et installer l’application **QuickStatus**. La procédure 6 présente quelques étapes supplémentaires pour le test de l’application, une fois celle-ci installée. 

<a name="pj15_StatusingApp_Deploying"> </a>

## <a name="deploying-the-quickstatus-app"></a>Déploiement de l’application QuickStatus

Il existe plusieurs façons de déployer une application sur une application web SharePoint telle que Project Web App. Le déploiement que vous utilisez varie selon que vous souhaitez publier l’application dans un catalogue SharePoint privé ou dans l’Office Store public, et que SharePoint soit installé en local ou qu’il s’agit d’une location en ligne. La procédure 5 montre comment déployer l’application **QuickStatus** sur une installation locale dans un catalogue d’applications privé. Pour plus d’informations, voir [Installer et gérer des applications pour SharePoint 2013](https://technet.microsoft.com/library/fp161232.aspx) et Publier des applications pour [SharePoint](https://msdn.microsoft.com/library/jj164070.aspx)
  
> [!NOTE]
> L’ajout d’une application à un catalogue SharePoint nécessite des autorisations d’administrateur SharePoint. 
  
### <a name="procedure-5-to-deploy-the-quickstatus-app"></a>Procédure 5. Pour déployer l’application QuickStatus

1. Dans Visual Studio, enregistrez tous les fichiers, puis cliquez avec le bouton droit sur le projet **QuickStatus** dans l’**Explorateur de solutions** et choisissez **Publier**.
    
2. Étant donné que l’application **QuickStatus** est hébergée par SharePoint, il existe très peu d’options de publication (voir la figure 8). Dans la boîte de dialogue **Publier des applications pour Office et SharePoint**, choisissez **Terminer**.
    
   **Figure 8. Publication de l’application QuickStatus**

   ![Utilisation de l’Assistant Publication](media/pj15_CreateStatusingApp_PublishWizard.gif "Utilisation de l’Assistant Publication")
  
3. Copiez le fichier QuickStatus.app à partir du répertoire vers un répertoire pratique sur l’ordinateur local (ou sur l’ordinateur SharePoint pour une  `~\QuickStatus\bin\Debug\app.publish\1.0.0.0` installation locale). 
    
4. Dans l’Administration centrale de SharePoint, choisissez **Applications** dans la barre de lancement rapide, puis choisissez **Gérer le catalogue d’applications**.
    
5. Si un catalogue d’applications n’existe pas, créez une collection de sites pour le catalogue d’applications, en suivant la section Configurer le site catalogue d’applications pour une  *application web*  dans Gérer le catalogue d’applications dans [SharePoint 2013](https://technet.microsoft.com/library/fp161234.aspx).
    
   Si un catalogue d’applications existe, accédez à l’URL du site sur la page Gérer le catalogue applications. Par exemple, dans les étapes suivantes, le site de catalogue d’applications est  `https://ServerName/sites/TestApps` .
    
6. Sur la page du catalogue d’applications, choisissez **Applications pour SharePoint** dans la barre de lancement rapide. Sur la page Applications pour SharePoint, sur l’onglet **FICHIERS** du ruban, choisissez **Télécharger un document**.
    
7. Dans la boîte de dialogue **Ajouter un document**, recherchez le fichier QuickStatus.app, ajoutez des commentaires pour la version, puis choisissez **OK**.
    
8. Lorsque vous ajoutez une application, vous pouvez également ajouter des informations locales pour la description de l’application, l’icône et d’autres informations. Dans la boîte de dialogue Applications pour **SharePoint - QuickStatus.app,** ajoutez les informations que vous souhaitez afficher pour l’application dans la collection de sites SharePoint. Par exemple, ajoutez les informations suivantes : 
    
   1. **Champ Description courte** : Tapez application de test d’état rapide.
    
   2. **Champ Description** : Tapez Application test pour mettre à jour le pourcentage achevé des tâches dans plusieurs projets.
    
   3. **Champs d’URL** d’icône : ajoutez une image de 96 x 96 pixels pour l’icône d’application aux ressources du site pour le catalogue d’applications. Par exemple, accédez à , choisissez contenu du site dans le menu déroulant `https://ServerName/sites/TestApps` **Paramètres,**  sélectionnez Ressources du site, puis ajoutez l’image quickStatusApp.png.  Cliquez avec le bouton droit sur l’élément **quickStatusApp**, choisissez **Propriétés**, puis copiez la valeur **Adresse (URL)** dans la boîte de dialogue **Propriétés**. Par exemple, copiez, puis collez la valeur  `https://ServerName/sites/TestApps/SiteAssets/QuickStatusApp.png` dans le champ d’adresse web **URL** de l’icône. Saisissez une description de l’icône, par exemple (comme dans la figure 9) entrezIcône de l’application QuickStatus. Vérifiez la validité de l’URL.
    
      **Figure 9. Ajout d’une URL d’icône pour l’application QuickStatus**

      ![Définition des propriétés dans SharePoint pour l’application](media/pj15_CreateStatusingApp_AddAppToSharePointSettings.gif "Définition des propriétés dans SharePoint pour l’application")
  
   4. Champ **Catégorie** : choisissez une catégorie existante ou spécifiez votre propre valeur. Par exemple, saisissez État.
    
      > [!NOTE]
      > Une catégorie nommée **État** sert uniquement à des fins de test. Une catégorie typique pour les applications de Project Server est **Gestion de projet**. 
  
   5. Champ **Nom de l’éditeur** : saisissez le nom de l’éditeur. Dans cet exemple, entrez Kit de développement logiciel (SDK) Project.
    
   6. **Champ activé** : pour rendre l’application visible pour les administrateurs de site Project Web App pour l’installation, activez **la case à** cocher Activée. 
    
   7. Les champs supplémentaires sont facultatifs. Par exemple, vous pouvez ajouter une URL de support technique et plusieurs images d’aide pour la page de détails d’application. Dans la figure 9, les champs **URL d’image 1** incluent l’URL de la capture d’écran de l’application et une description de cette capture d’écran. 
    
   8. Dans la boîte de dialogue Applications **pour SharePoint - QuickStatus.app,** choisissez **Enregistrer.** Dans la figure  9, l’élément Mise à jour rapide de l’état dans la bibliothèque Applications pour  SharePoint est extrait pour modification. Ainsi, sous l’onglet **MODIFIER** du ruban de la boîte de dialogue, vous devez choisir Archiver pour terminer le processus (voir la figure 10). 
    
      **Figure 10. L’application QuickStatus est ajoutée dans la bibliothèque Applications pour SharePoint.**

      ![L’application QuickStatus est ajoutée à SharePoint](media/pj15_CreateStatusingApp_AddAppToSharePoint.gif "L’application QuickStatus est ajoutée à SharePoint")
  
9. Dans Project Web App, dans le menu déroulant **Paramètres,** choisissez **Ajouter une application.** Sur la page Vos applications, dans la barre de lancement rapide, choisissez **De votre organisation**, puis **Détails de l’application** pour l’application **Mise à jour de l’état rapide**. La figure 11 montre la page de détails avec l’icône d’application, la capture d’écran et les informations que vous avez ajoutées à l’étape précédente. 
    
   **Figure 11. Utilisation de la page de détails Mise à jour de l’état rapide dans Project Web App**

   ![Ajout de l’application QuickStatus à Project Web App](media/pj15_CreateStatusingApp_AddAppToPWA.gif "Ajout de l’application QuickStatus à Project Web App")
  
10. Sur la page de détails Mise à jour de l’état rapide, choisissez **AJOUTER**. Project Web App affiche une boîte de dialogue qui répertorie les opérations que l’application QuickStatus peut effectuer (voir figure 12). La liste des opérations est dérivée des éléments **AppPermissionRequest** du fichier AppManifest.xml. 
    
    **Figure 12. Vérification de la confiance accordée à l’application QuickStatus**

    ![Vérification de l’approbation pour l’application QuickStatus](media/pj15_CreateStatusingApp_AddAppToPWA2Trust.gif "Vérification de l’approbation pour l’application QuickStatus")
  
11. Dans la boîte de dialogue **Faites-vous confiance à la mise à jour de l’état rapide ?**, choisissez **Approuver**. L’application est ajoutée à la page Contenu du site Project Web App (voir la figure 13).
    
    **Figure 13. Affichage de l’application QuickStatus sur la page Contenu du site**

    ![Affichage de l’application QuickStatus dans le contenu du site](media/pj15_CreateStatusingApp_AddAppToPWA3.gif "Affichage de l’application QuickStatus dans le contenu du site")
  
Sur la page Contenu du site, vous pouvez sélectionner l’icône **Mise à jour de l’état rapide** pour exécuter l’application.

> [!NOTE]
> Pour obtenir des commandes supplémentaires qui fournissent des informations sur l’application, dans la page Contenu du site, choisissez la région qui contient le nom de la mise à jour de l’état rapide et les ellipses (...).  Vous pouvez consulter la page À propos de l’application, afficher la page Détails de l’application qui contient des informations sur les erreurs de l’application, consulter la page autorisations de l’application ou supprimer l’application de Project Web App. 
  
Dans la page Tâches de Project Web App (voir figure 14), le bouton **QuickStatus** doit être activé sur le ruban. Si le bouton **État rapide** est désactivé, essayez les actions décrites dans la remarque de la figure 7. 

**Figure 14. Lancement de l’application QuickStatus à partir de l’onglet TÂCHES**

![Lancement de l’application QuickStatus à partir de l’onglet TÂCHES](media/pj15_CreateStatusingApp_TasksRibbon.gif "Lancement de l’application QuickStatus à partir de l’onglet TÂCHES")
  
La procédure 6 décrit certains tests à effectuer avec l’application QuickStatus.

<a name="pj15_StatusingApp_Testing"> </a>

## <a name="testing-the-quickstatus-app"></a>Test de l’application QuickStatus

Chaque opération qu’un utilisateur peut essayer dans l’application **QuickStatus** doit être testée sur une installation de test de Project Server avant de déployer l’application sur un serveur de production ou sur un client de production de Project Online. Une installation de test vous permet de modifier et supprimer les affectations pour les utilisateurs sans répercussion aucune sur les projets réels. Le test doit également impliquer plusieurs utilisateurs ayant différents ensembles d’autorisations, comme un administrateur, un responsable de projet et un membre d’équipe. Des tests minutieux peuvent révéler des modifications devant être effectuées dans l’application, qui n’ont pas été repérées lors du test effectué pendant le développement. La procédure 6 répertorie plusieurs tests pour l’application **QuickStatus**, cette série de tests n’est pas exhaustive. 
  
### <a name="procedure-6-to-test-the-quickstatus-app"></a>Procédure 6. Pour tester l’application QuickStatus

1. Exécutez l’application **QuickStatus** sur laquelle l’utilisateur n’a aucune affectation. L’application doit afficher un message bleu en bas de la page, par exemple, **Le nom d’utilisateur ne dispose d’aucune affectation**.
    
   Choisissez **Mettre à jour**. Le message devient alors vert et indique **Les affectations ont été mises à jour**.
    
   > [!NOTE]
   > Le comportement de l’application  doit être modifié afin que le bouton Mettre à jour soit désactivé lorsqu’il n’y a aucune affectation. 
  
2. Exécutez l’application dans laquelle l’utilisateur a plusieurs affectations dans plusieurs projets différents et certaines affectations ne sont pas terminées. Notez l’apparence de l’application et effectuez les actions suivantes (voir la figure 15) :
    
   1. La **fonction onGetAssignmentsSuccess** crée une ligne dans le tableau pour chaque affectation de l’utilisateur actuel. Le nom du projet ne s’affiche qu’une seule fois, en gras, pour la première affectation de chaque projet. 
    
   2. Cochez la case dans **l’en-tête** de colonne Nom de la tâche. Le handler d’événement click d’en-tête de tableau permet d’effacer toutes les autres cases à cocher des lignes de tâche. 
    
   3. Sélectionnez toutes les tâches. Le handler d’événement Click de chaque ligne détermine si toutes les lignes sont sélectionnées et, si tel est le cas, sélectionne l’en-tête de **colonne** Nom de la tâche. 
    
   4. Clear all of the check boxes again, and then select one assignment that has some remaining work. Par exemple, la figure 15 montre que la tâche supérieure T1 a 20 % de travail restant à accomplir.
    
   5. Dans la zone de texte Définir **le pourcentage d’achevé,** tapez 80, puis choisissez Mettre à **jour.** Le bas de la page doit afficher un message vert, **affectations ont été mises à jour**.
    
      **Figure 15. Mise à jour d’une affectation dans l’application QuickStatus**

      ![Mise à jour d’une affectation dans l’application QuickStatus](media/pj15_CreateStatusingApp_Testing1Update.gif "Mise à jour d’une affectation dans l’application QuickStatus")
  
3. Choisissez **Actualiser** (voir figure 16). Toutes les tâches sont sélectionnées à nouveau et la tâche supérieure affiche 80 % d’achevé. 
    
      **Figure 16. Actualisation de la page Mise à jour rapide de l’état**

      ![Actualisation de la page QuickStatus](media/pj15_CreateStatusingApp_Testing2Refresh.gif "Actualisation de la page QuickStatus")
  
4. Effacer toutes les cases à cocher, puis sélectionner une autre tâche. Par exemple, **sélectionnez Nouvelle tâche à partir de PWA.** Laissez la **zone de** texte définir le  pourcentage de texte achevé vide, supprimez tout le texte dans la colonne % achevé pour la tâche sélectionnée, puis choisissez Mettre à **jour**. Étant donné que les deux zones de texte sont vides, l’application affiche un message d’erreur rouge (voir figure 17).
    
      **Figure 17. Test du message d’erreur**

      ![Test du message d’erreur](media/pj15_CreateStatusingApp_Testing3Error.gif "Test du message d’erreur")
  
5. Mettez à jour la tâche précédente à 80 % terminée, puis choisissez **Quitter**. La **fonction exitToPwa** change l’emplacement de la fenêtre du navigateur en page Tâches dans l’application hôte SharePoint (autrement dit, l’URL change en https://ServerName/pwa/Tasks.aspx) . La figure 18 montre que les tâches **T1** et Nouvelle tâche de **PWA** indiquent chacune 80 % d’achevé. 
    
      **Figure 18. Vérification de la mise à jour des tâches dans Project Web App**

      ![Vérification des tâches de mises à jour dans Project Web App](media/pj15_CreateStatusingApp_TasksUpdatedInPWA.gif "Vérification des tâches de mises à jour dans Project Web App")
  
6. Avant que l’état mis à jour ne s’affiche dans Project Professionnel 2013, les modifications doivent être soumises pour approbation, puis approuvées par le responsable de projet.
    
Le test révèle plusieurs autres modifications qui doivent être apportées dans l’application **QuickStatus** pour une meilleure utilisation. Par exemple :

- Il doit y avoir des vérifications d’erreur supplémentaires et la validation des valeurs de zone de texte. Actuellement, un utilisateur peut entrer une valeur non numérique ou une valeur négative pour le pourcentage achevé, ce qui entraîne un message d’erreur non convivial. Par exemple, avec une valeur négative, le message d’erreur est Error **updating assignments: PJClientCallableException: StatusingSetDataValueInvalid**.
    
- Le message d’erreur pour les zones de texte vides peut lister le projet et la tâche, en plus du numéro de ligne.
    
- Le message de réussite peut inclure une liste des tâches mises à jour . ou si la **fonction updateAssignments** réussit, elle peut effectuer une actualisation automatique de la page et afficher des tâches ou des pourcentages mis à jour dans une couleur et une police en gras différentes. 
    
- Pour éviter un tableau très important, le tableau des affectations doit être limité aux tâches qui sont inférieures à 100 %. Vous pouvez également ajouter une option pour afficher toutes les tâches. Ce problème peut également être résolu à l’aide d’une grille basée sur jQuery au lieu d’une table, où vous pouvez facilement implémenter le filtrage et la pagination de grille.
    
- Étant donné que l’application **QuickStatus** ne soumet pas l’état, l’icône État rapide  sous l’onglet  **TÂCHES** du  ruban serait plus logiquement la première icône du groupe Tâches, plutôt que la dernière icône du groupe Envoyer. 
    
- Étant donné que la fonction **onGetAssignmentsSuccess** initialise le texte du bouton **btnSubmitUpdate,** mais que les autres valeurs de texte du bouton sont initialisées au format HTML, la page reste dans un état partiellement initialisé pendant que la fonction **getAssignments** s’exécute. Les boutons de la page apparaissent plus cohérents si les valeurs de texte sont toutes initialisées au format HTML. 
    
Plus important encore, l’approche que l’application **QuickStatus** utilise, où elle change le pourcentage achevé pour les affectations, doit être révisée dans une application de production. Pour plus d’informations, voir la section [Étapes suivantes.](#pj15_StatusingApp_NextSteps) 

<a name="pj15_StatusingApp_Example"> </a>

## <a name="example-code-for-the-quickstatus-app"></a>Exemple de code pour l’application QuickStatus

### <a name="defaultaspx-file"></a>Fichier Default.aspx

Le code suivant se trouve dans  `Pages\Default.aspx` le fichier du projet **QuickStatus** : 
  
```HTML
    <%-- The following lines are ASP.NET directives needed when using SharePoint components --%>
    <%@ Page Inherits="Microsoft.SharePoint.WebPartPages.WebPartPage, Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" MasterPageFile="~masterurl/default.master" Language="C#" %>
    <%@ Register TagPrefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%@ Register TagPrefix="WebPartPages" Namespace="Microsoft.SharePoint.WebPartPages" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%@ Register TagPrefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%-- The markup and script in the following Content element will be placed in the <head> of the page.
        For production deployment, change the .debug.js JavaScript references to .js. --%>
    <asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">
    <script type="text/javascript" src="../Scripts/jquery-1.7.1.min.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.runtime.debug.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.debug.js"></script>
    <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
    <!-- CSS styles -->
    <link rel="Stylesheet" type="text/css" href="../Content/App.css" />
    <!-- Add your JavaScript to the following file -->
    <script type="text/javascript" src="../Scripts/App.js"></script>
    </asp:Content>
    <%-- The markup and script in the following Content element will be placed in the <body> of the page --%>
    <asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">
    <form>
        <fieldset>
        <legend>Select assigned tasks</legend>
        <table id="assignmentsTable">
            <caption id="tableCaption">Replace caption</caption>
            <thead>
            <tr id="headerRow">
                <th>Project name</th>
                <th><input type="checkbox" id="headercheckbox" checked="checked" />Task name</th>
                <th>Actual work</th>
                <th>% complete</th>
                <th>Remaining work</th>
                <th>Due date</th>
            </tr>
            </thead>
        </table>
        </fieldset>
        <div id="inputPercentComplete" >
        Set percent complete for all selected assignments, or leave this
        <br /> field blank and set percent complete for individual assignments: 
        <input type="text" name="percentComplete" id="pctComplete" size="4"  maxlength="4" />
        </div>
        <div id="submitResult">
        <p><button id="btnSubmitUpdate" type="button" class="bottomButtons" ></button></p>
        <p id="message"></p>
        </div>
        <div id="refreshPage">
        <p><button id="btnRefresh" type="button" class="bottomButtons" >Refresh</button></p>
        </div>
    <div id="exitPage">
        <p><button id="btnExit" type="button" class="bottomButtons" >Exit</button></p>
    </div>
    </form>
    </asp:Content>
```

<br/>

### <a name="appjs-file"></a>App.js fichier

Le code suivant se trouve dans  `Scripts\App.js` le fichier du projet **QuickStatus** : 
  
```js
    var projContext;
    var pwaWeb;
    var projUser;
    // This code runs when the DOM is ready and creates a ProjectContext object.
    // The ProjectContext object is required to use the JSOM for Project Server.
    $(document).ready(function () {
        projContext = PS.ProjectContext.get_current();
        pwaWeb = projContext.get_web();
        getUserInfo();
        getAssignments();
        // Bind a click event handler to the table header check box, which sets the row check boxes
        // to the selected state of the header check box, and sets the results message to an empty string.
        $('#headercheckbox').live('click', function (event) {
            $('input:checkbox:not(#headercheckbox)').attr('checked', this.checked);
            $get("message").innerText = "";
        });
        // Bind a click event handler to the row check boxes. If any row check box is cleared, clear
        // the header check box. If all of the row check boxes are selected, select the header check box.
        $('input:checkbox:not(#headercheckbox)').live('click', function (event) {
            var isChecked = true;
            $('input:checkbox:not(#headercheckbox)').each(function () {
                if (this.checked == false) isChecked = false;
                $get("message").innerText = "";
            });
            $("#headercheckbox").attr('checked', isChecked);
        });
    });
    // Get information about the current user.
    function getUserInfo() {
        projUser = pwaWeb.get_currentUser();
        projContext.load(projUser);
        projContext.executeQueryAsync(onGetUserNameSuccess,
            // Anonymous function to execute if getUserInfo fails.
            function (sender, args) {
                alert('Failed to get user name. Error: ' + args.get_message());
        });
    }
    // This function is executed if the getUserInfo call is successful.
    // Replace the contents of the 'caption' paragraph with the project user name.
    function onGetUserNameSuccess() {
        var prefaceInfo = 'Assignments for ' + projUser.get_title();
        $('#tableCaption').text(prefaceInfo);
    }
    // Get the collection of assignments for the current user.
    function getAssignments() {
        assignments = PS.EnterpriseResource.getSelf(projContext).get_assignments();
        // Register the request that you want to run on the server. The optional "Include" parameter 
        // requests only the specified properties for each assignment in the collection.
        projContext.load(assignments,
            'Include(Project, Name, ActualWork, ActualWorkMilliseconds, PercentComplete, RemainingWork, Finish, Task)');
        // Run the request on the server.
        projContext.executeQueryAsync(onGetAssignmentsSuccess,
            // Anonymous function to execute if getAssignments fails.
            function (sender, args) {
                alert('Failed to get assignments. Error: ' + args.get_message());
            });
    }
    // Get the enumerator, iterate through the assignment collection, 
    // and add each assignment to the table.
    function onGetAssignmentsSuccess(sender, args) {
        if (assignments.get_count() > 0) {
            var assignmentsEnumerator = assignments.getEnumerator();
            var projName = "";
            var prevProjName = "3D2A8045-4920-4B31-B3E7-9D0C5195FC70"; // Any unique name.
            var taskNum = 0;
            var chkTask = "";
            var txtPctComplete = "";
            // Constants for creating input controls in the table.
            var INPUTCHK = '<input type="checkbox" class="chkTask" checked="checked" id="chk';
            var LBLCHK = '<label for="chk';
            var INPUTTXT = '<input type="text" size="4"  maxlength="4" class="txtPctComplete" id="txt';
            while (assignmentsEnumerator.moveNext()) {
                var statusAssignment = assignmentsEnumerator.get_current();
                projName = statusAssignment.get_project().get_name();
                // Get an integer value for the number of milliseconds of actual work, such as 3600000.
                var actualWorkMilliseconds = statusAssignment.get_actualWorkMilliseconds();
                // Get a string value for the assignment actual work, such as "1h". Not used here.
                var actualWork = statusAssignment.get_actualWork();                         
                if (projName === prevProjName) {
                    projName = "";
                }
                prevProjName = statusAssignment.get_project().get_name();
                // Create a row for the assignment information.
                var row = assignmentsTable.insertRow();
                taskNum++;
                // Create an HTML string with a check box and task name label, for example:
                //     <input type="checkbox" class="chkTask" checked="checked" id="chk1" /> 
                //     <label for="chk1">Task 1</label>
                chkTask = INPUTCHK + taskNum + '" /> ' + LBLCHK + taskNum + '">'
                    + statusAssignment.get_name() + '</label>';
                txtPctComplete = INPUTTXT + taskNum + '" />';
                // Insert cells for the assignment properties.
                row.insertCell().innerHTML = '<strong>' + projName + '</strong>';
                row.insertCell().innerHTML = chkTask;
                row.insertCell().innerText = actualWorkMilliseconds / 3600000 + 'h';
                row.insertCell().innerHTML = txtPctComplete;
                row.insertCell().innerText = statusAssignment.get_remainingWork();
                row.insertCell().innerText = statusAssignment.get_finish();
                // Initialize the percent complete cell.
                $get("txt" + taskNum).innerText = statusAssignment.get_percentComplete() + '%'
            }
        }
        else {
            $('p#message').attr('style', 'color: #0f3fdb');     // Blue text.
            $get("message").innerText = projUser.get_title() + ' has no assignments'
        }
        // Initialize the button properties.
        $get("btnSubmitUpdate").onclick = function() { updateAssignments(); };
        $get("btnSubmitUpdate").innerText = 'Update';
        $get('btnRefresh').onclick = function () { window.location.reload(true); };
        $get('btnExit').onclick = function () { exitToPwa(); };
    }
    // Update all selected assignments. If the bottom percent complete field is blank,
    // use the value in the % complete field of each selected row in the table.
    function updateAssignments() {
        // Get percent complete from the bottom text box.
        var pctCompleteMain = getNumericValue($('#pctComplete').val()).trim();
        var pctComplete = pctCompleteMain;
        var assignmentsEnumerator = assignments.getEnumerator();
        var taskNum = 0;
        var taskRow = "";
        var indexPercent = "";
        var doSubmit = true;
        while (assignmentsEnumerator.moveNext()) {
            var pctCompleteRow = "";
            taskRow = "chk" + ++taskNum;
            if ($get(taskRow).checked) {
                var statusAssignment = assignmentsEnumerator.get_current();
                if (pctCompleteMain === "") {
                    // Get percent complete from the text box field in the table row.
                    pctCompleteRow = getNumericValue($('#txt' + taskNum).val());
                    pctComplete = pctCompleteRow;
                }
                // If both percent complete fields are empty, show an error.
                if (pctCompleteMain === "" && pctCompleteRow === "") {
                    $('p#message').attr('style', 'color: #e11500');     // Red text.
                    $get("message").innerHTML =
                        '<b>Error:</b> Both <i>Percent complete</i> fields are empty, in row '
                        + taskNum
                        + ' and in the bottom textbox.<br/>One of those fields must have a valid percent.'
                        + '<p>Please refresh the page and try again.</p>';
                    doSubmit = false;
                    taskNum = 0;
                    break;
                }
                if (doSubmit) statusAssignment.set_percentComplete(pctComplete);
            }
        } 
        // Save and submit the assignment updates.
        if (doSubmit) {
            assignments.update();
            assignments.submitAllStatusUpdates();
            projContext.executeQueryAsync(function (source, args) {
                $('p#message').attr('style', 'color: #0faa0d');     // Green text.
                $get("message").innerText = 'Assignments have been updated.';
            }, function (source, args) {
                $('p#message').attr('style', 'color: #e11500');     // Red text.
                $get("message").innerText = 'Error updating assignments: ' + args.get_message();
            });
        }
    }
    // Get the numeric part for percent complete, from a string. 
    // For example, with "20 %", return "20".
    function getNumericValue(pctComplete) {
        pctComplete = pctComplete.trim();
        pctComplete = pctComplete.replace(/ /g, "");    // Remove interior spaces.
        indexPercent = pctComplete.indexOf('%', 0);
        if (indexPercent > -1) pctComplete = pctComplete.substring(0, indexPercent);
        return pctComplete;
    }
    // Exit the QuickStatus page and go back to the Tasks page in Project Web App.
    function exitToPwa() {
        // Get the SharePoint host URL, which is the top page of PWA, and add the Tasks page.
        var spHostUrl = decodeURIComponent(getQueryStringParameter('SPHostUrl'))
                        + "/Tasks.aspx";
        // Set the top window for the QuickStatus IFrame to the Tasks page.
        window.top.location.href = spHostUrl;
    }
    // Get a specified query string parameter from the {StandardTokens} URL option string.
    function getQueryStringParameter(urlParameterKey) {
        var docUrl = document.URL;
        var params = docUrl.split('?')[1].split('&');
        for (var i = 0; i < params.length; i++) {
            var theParam = params[i].split('=');
            if (theParam[0] == urlParameterKey)
                return decodeURIComponent(theParam[1]);
        }
    }
```

<br/>

### <a name="appcss-file"></a>Fichier App.css

Le code CSS suivant se trouve dans le  `Content\App.css` fichier du **projet QuickStatus** : 
  
```css
    /* Custom styles for the QuickStatus app. */
    /*============= Table elements ========================================*/
    table {
        width: 90%;
    }
    caption {
        font-size: 16px;
        padding-bottom: 5px;
        font-weight: bold;
        color: gray;
    }
    table th {
        background-color: gray;
        color: white;
    }
    table td, th {
        width: auto;
        text-align: left;
        padding: 2px;
        border: solid 1px whitesmoke;
        color: gray;
    }
    /*=== Class for check boxes added to rows 
    */
    .chkTask {
        width: 12px;
        height: 12px;
        color: gray;
    }
    /*========== DIV id for the Percent Complete text box ================*/
    #inputPercentComplete {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 20px;
        margin-left: 30px;
    }
    /*========== DIV id for the Submit Result button ====================*/
    #submitResult {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
    }
    /*========== DIV id for the Refresh Page button ====================*/
    #refreshPage {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
        margin-left: 120px;
    }
    /*========== DIV id for the Exit Page button ====================*/
    #exitPage {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
        margin-left: 240px;
    }
    /*========== Class for the buttons at the bottom of the page =======*/
    .bottomButtons {
        color: gray;
        font-weight: bold; 
        font-size: 12px; 
        border-color: darkgreen;
        border-width: thin;
    }
```

<br/>

### <a name="elementsxml-file-for-the-ribbon"></a>Elements.xml fichier pour le ruban

La définition XML suivante, pour le bouton ajouté sous l’onglet **TÂCHES** du ruban, se trouve dans le fichier du  `RibbonQuickStatusAction\Elements.xml` projet **QuickStatus** : 
  
```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="http://schemas.microsoft.com/sharepoint/">
    <CustomAction Id="21ea3aaf-79e5-4aac-9479-8eef14b4d9df.RibbonQuickStatusAction"
                    Location="CommandUI.Ribbon">
        <CommandUIExtension>
        <!-- 
        Add a button that invokes the QuickStatus app. The Quick Status button is displayed as  
        the third control in the Page group (the group title is "Submit").
        -->
        <CommandUIDefinitions>
            <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
            <Button Id="Ribbon.ContextualTabs.MyWork.Home.Page.QuickStatus"
                    Alt="Quick Status app"
                    Sequence="30"
                    Command="Invokae_QuickStatus"
                    LabelText="Quick Status"
                    TemplateAlias="o1"
                    Image16by16="_layouts/15/1033/images/ps16x16.png" 
                    Image16by16Left="-80"
                    Image16by16Top="-144"
                    Image32by32="_layouts/15/1033/images/ps32x32.png" 
                    Image32by32Left="-32"
                    Image32by32Top="-288" 
                    ToolTipTitle="Quick Status"
                    ToolTipDescription="Run the QuickStatus app" />
            </CommandUIDefinition>
        </CommandUIDefinitions>
        <CommandUIHandlers>
            <CommandUIHandler Command="Invoke_QuickStatus"
                            CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
        </CommandUIHandlers>
        </CommandUIExtension >
    </CustomAction>
    </Elements>
```

<br/>

### <a name="appmanifestxml-file"></a>AppManifest.xml fichier

Voici le XML pour le manifeste d’application du projet **QuickStatus,** qui inclut les deux étendues de demande d’autorisation nécessaires pour mettre à jour l’état d’affectation de l’utilisateur de l’application dans plusieurs projets : 
  
```XML
    <?xml version="1.0" encoding="utf-8" ?>
    <!--Created:cb85b80c-f585-40ff-8bfc-12ff4d0e34a9-->
    <App xmlns="http://schemas.microsoft.com/sharepoint/2012/app/manifest"
        Name="QuickStatus"
        ProductID="{bbc497e7-1221-4d7b-a0ae-141a99546008}"
        Version="1.0.0.0"
        SharePointMinVersion="15.0.0.0"
    >
    <Properties>
        <Title>Quick Status Update</Title>
        <StartPage>~appWebUrl/Pages/Default.aspx?{StandardTokens}</StartPage>
    </Properties>
    <AppPrincipal>
        <Internal />
    </AppPrincipal>
    <AppPermissionRequests>
        <AppPermissionRequest Scope="https://sharepoint/projectserver/statusing" Right="SubmitStatus" />
        <AppPermissionRequest Scope="https://sharepoint/projectserver/projects" Right="Read" />
    </AppPermissionRequests>
    </App>
```

<br/>

### <a name="appiconpng-file"></a>AppIcon.png fichier

La solution Visual Studio complète pour l’application **QuickStatus** inclut un fichier AppIcon.png personnalisé. La solution sera incluse dans le téléchargement du SDK Project 2013. 

<a name="pj15_StatusingApp_NextSteps"> </a>

## <a name="next-steps"></a>Étapes suivantes

**L’application QuickStatus** est un exemple relativement simple de la façon d’écrire des applications qui peuvent être installées sur Project Server 2013 et Project Online. La section [Test de l’application QuickStatus](#pj15_StatusingApp_Testing) répertorie plusieurs améliorations qui peuvent être apportées pour une meilleure utilisation. **L’application QuickStatus** utilise les fonctions JavaScript pour mettre à jour l’état d’affectation pour Project Web App. Toutefois, il n’est pas recommandé de modifier le pourcentage d’affectation achevé. Une autre approche consiste à mettre à jour la date de début réelle et la durée restante des tâches affectées. Pour plus d’informations sur les problèmes, voir [Mettre à jour mieux](https://www.mpug.com/articles/update-better) dans le bulletin d’informations MPUG. 

<a name="pj15_StatusingApp_AdditionalResources"> </a>

## <a name="see-also"></a>Voir aussi

- [Tâches de programmation Project Server](project-programming-tasks.md)
- [Compléments](https://msdn.microsoft.com/library/jj163230.aspx)
- [Gestion des mises à jour de tâches dans Project Web App](https://technet.microsoft.com/library/hh767481%28v=office.14%29.aspx)
- [Créer des actions personnalisées à déployer avec les compléments SharePoint](https://msdn.microsoft.com/library/jj163954.aspx)
    

