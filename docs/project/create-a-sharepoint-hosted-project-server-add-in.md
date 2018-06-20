---
title: Créer un complément Project Server hébergé sur SharePoint
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: bb9c3c00-7121-41e1-9db3-75550d040ba8
description: Les trois types d’applications que vous pouvez créer pour Project Online (auto-hébergement, hébergé par le fournisseur et hébergée par SharePoint), est la plus simple créer et déployer l’application hébergée par SharePoint.
ms.openlocfilehash: 135a6cd330224041db213e0408735209056d34af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787825"
---
# <a name="create-a-sharepoint-hosted-project-server-add-in"></a>Créer un complément Project Server hébergé sur SharePoint

Les trois types d’applications que vous pouvez créer pour Project Online (auto-hébergement, hébergé par le fournisseur et hébergée par SharePoint), est la plus simple créer et déployer l’application hébergée par SharePoint. N’est pas le cas d’une application hébergée par SharePoint nécessitent une authentification OAuth et ne pas utiliser Azure ou nécessitent une maintenance d’un site local pour les ressources hébergées par un fournisseur. Le modèle **d’application pour SharePoint 2013** dans Visual Studio est une structure pratique pour le développement d’applications qui peuvent être publiées et vendues dans l’Office Store ou déployées dans un catalogue d’applications privé sur SharePoint. 
  
Dans le projet, état est un processus dans lequel un membre d’équipe permettre utiliser la page tâches dans Project Web App pour envoyer l’état d’une tâche affectée, telles que le nombre d’heures travaillées chaque jour de la semaine passé à travailler sur la tâche. Le propriétaire de l’affectation (généralement, le responsable de projet) permettre approuver ou rejeter l’état. Lorsque l’état est approved, Project recalcule la planification. L’application **QuickStatus** affiche les tâches affectées, où l’utilisateur peut mettre à jour le pourcentage d’achèvement rapidement et soumettre l’état des affectations sélectionnées pour approbation. Bien que la page tâches dans Project Web App a beaucoup plus de fonctionnalités, l’application **QuickStatus** est un exemple qui fournit une interface simplifiée. 
  
L’application **QuickStatus** est un exemple pour les développeurs ; elle n’est pas destinée à utiliser dans un environnement de production. Le principal objectif consiste à afficher un exemple de développement d’applications pour Project Online, ne pas à créer une application d’état entièrement fonctionnelle. Pour une meilleure approche pour un état, voir la recommandation dans les [étapes suivantes](#pj15_StatusingApp_NextSteps).
  
Pour obtenir des informations générales sur l’état, voir [l’avancement des tâches](https://support.office.com/article/Find-information-about-Project-Server-2013-8b08a414-15a7-4076-b2db-c90d0214ea7f?ui=en-US&rs=en-US&ad=US#BKMK_TaskProgress). Pour plus d’informations sur le développement de compléments pour SharePoint et Project Server, voir [SharePoint Add-ins](http://msdn.microsoft.com/en-us/library/jj163230.aspx).

<a name="pj15_StatusingApp_Prerequisites"> </a>

## <a name="prerequisites-for-creating-an-app-for-project-server-2013"></a>Conditions préalables à la création d’une application pour Project Server 2013

Pour développer des applications relativement simples qui peuvent être déployées pour Project Online ou à une installation locale de Project Server 2013, vous pouvez utiliser la Napa, qui fournissent un environnement de développement en ligne. Pour les applications plus complexes, modifier le ruban Project Web App et faciliter le débogage pendant le développement, vous pouvez utiliser Visual Studio 2012 ou Visual Studio 2013. Par exemple, avec une installation locale, vous pouvez vérifier manuellement les tables de données brouillons les modifications apportées à la base de données Project Server. Cet article explique comment effectuer le développement d’applications avec Visual Studio.
  
Le développement d’applications Project Server avec Visual Studio nécessite les éléments suivants :
  
- Assurez-vous d’avoir installé les mises à jour Windows et les Service Packs les plus récents sur votre ordinateur de développement local. Le système d’exploitation peut être Windows 7, Windows 8, Windows Server 2008 ou Windows Server 2012.
    
- Vous devez disposer d’un ordinateur équipé de SharePoint Server 2013 et Project Server 2013 est installé, où l’ordinateur est configuré pour l’isolation de l’application et chargement de version test des applications. Chargement de version test permet à Visual Studio Installer temporairement l’application pour le débogage. Vous pouvez utiliser une installation locale de SharePoint et Project Server. Pour plus d’informations, consultez [configurer un environnement de développement local pour les applications pour SharePoint](http://msdn.microsoft.com/en-us/library/fp179923%28Office.15%29.aspx).
    
   > [!NOTE]
   > Pour une installation locale, configurez une application isolé domaine de *avant de* créer un catalogue d’applications d’entreprise. 
  
- L’ordinateur de développement peut être un ordinateur distant qui possède des outils de développement Office pour Visual Studio 2012 est installé. Vérifiez que vous avez installé la version la plus récente ; consultez la section *Outils* les [téléchargements d’applications pour Office et SharePoint](http://msdn.microsoft.com/en-us/office/apps/fp123627.aspx).
    
- Vérifiez que l’instance Project Web App vous utiliserez pour le développement et le test est accessible dans le navigateur.
    
Pour plus d’informations sur l’utilisation des outils en ligne, consultez [configurer un environnement de développement d’applications pour SharePoint dans Office 365](http://msdn.microsoft.com/en-us/library/fp161179.aspx). Pour une procédure pas à pas de création d’une application simple pour Project Server qui utilise les outils en ligne, voir la série de blog EPMSource, [Création de votre première application Project Server](http://epmsource.com/2012/11/20/building-your-first-project-server-app-part-zerothe-introduction/).

<a name="pj15_StatusingApp_UsingVisualStudio"> </a>

## <a name="using-visual-studio-to-create-a-project-server-app"></a>Utilisation de Visual Studio pour créer une application Project Server

Outils de développement Office pour Visual Studio 2012 inclut un modèle pour les applications SharePoint qui peut être utilisé avec Project Server 2013. Lorsque vous créez une solution d’application, la solution comprend les fichiers suivants pour votre code personnalisé :
  
- **AppManifest.xml** contient des paramètres pour le titre de l’application, étendue de demande d’autorisation et d’autres propriétés. Procédure 1 inclut des étapes pour définir les propriétés à l’aide du Concepteur de manifeste. 
    
- **Default.aspx** dans le dossier Pages correspond à la page principale de l’application. Procédure 2 montre comment ajouter du contenu HTML5 pour l’application **QuickStatus** . 
    
- **App.js** dans le dossier Scripts est le fichier principal pour le code JavaScript personnalisé. Procédure 3 décrit le code JavaScript pour l’application **QuickStatus** . 
    
   Si vous ajoutez des contrôles comme un jQuery-based une grille ou un sélecteur de dates, vous pouvez ajouter des références à des fichiers JavaScript supplémentaires dans le fichier Default.aspx.
    
- **App.css** dans le dossier de contenu est le fichier principal pour les styles CSS3 personnalisés. Procédure 2 et 3 de la procédure contiennent des informations sur les feuilles de style en cascade pour l’application **QuickStatus** . Vous pouvez ajouter des références aux fichiers CSS supplémentaires dans le fichier Default.aspx. 
    
- **AppIcon.png** dans le dossier Images est l’icône de 96 x 96 l’application s’affiche dans l’Office Store ou le catalogue d’applications. 
    
Pour modifier le ruban Project Web App, vous pouvez ajouter une action personnalisée du ruban. La section [exemple de code pour l’application QuickStatus](#pj15_StatusingApp_Example) inclut le code complet pour les fichiers Default.aspx, App.js, App.css, Elements.xml et AppManifest.xml modifiés. 
  
### <a name="procedure-1-to-create-an-app-project-in-visual-studio"></a>Procédure 1. Pour créer un projet d’application dans Visual Studio

1. Exécutez Visual Studio 2012 en tant qu’administrateur, puis sélectionnez **Nouveau projet** dans la page de démarrage. 
    
2. Dans la boîte de dialogue **Nouveau projet** , développez les **modèles**, **Visual c#** et nœuds **Office/SharePoint** , puis sélectionnez **applications**. Utilisez la valeur par défaut de **.NET Framework 4.5** dans la liste déroulante du framework cible en haut du volet central et puis sélectionnez **application pour SharePoint 2013** (voir Figure 1). 
    
3. Dans le champ **nom** , tapez QuickStatus, accédez à l’emplacement où vous souhaitez enregistrer l’application, puis cliquez sur **OK**.
    
   **La figure 1. Création d’un projet Application Server dans Visual Studio**

   ![Création d’un projet Application Server dans Visual Studio] (media/pj15_CreateStatusingApp_NewProject.gif "Création d’un projet Application Server dans Visual Studio")
  
4. Dans la boîte de dialogue **nouvelle application pour SharePoint** , renseignez les trois champs suivants : 
    
   - Dans la zone de texte, tapez le nom que vous souhaitez que l’application à afficher dans Project Web App. Par exemple, tapez mise à jour de statut rapide.
    
   - Pour le site à utiliser pour le débogage, tapez l’URL de l’instance Project Web App. Par exemple, tapez `https://ServerName/ProjectServerName` (remplacez _ServerName_ et _ProjectServerName_ avec vos propres valeurs), puis cliquez sur **Valider**. Si tout se passe bien, Visual Studio affiche **connexion réussie**. Si vous obtenez un message d’erreur, vérifiez que l’URL Project Web App est correct et que l’ordinateur Project Server est configuré pour l’isolation de l’application et chargement de version test des applications. Pour plus d’informations, voir la section [conditions requises pour la création d’une application pour Project Server 2013](#pj15_StatusingApp_Prerequisites) . 
    
   - Dans la liste déroulante **Comment voulez-vous héberger votre application pour SharePoint** , choisissez **hébergée par SharePoint**.
    
   > [!CAUTION]
   > Si vous choisissez le type de projet par défaut **hébergée** par inadvertance, Visual Studio crée deux projets dans la solution : un projet **QuickStatus** et un projet **QuickStatusWeb** . Si vous voyez deux projets, supprimer cette solution et recommencez. 
  
5. Cliquez sur **OK** pour créer la solution **QuickStatus** , project **QuickStatus** et fichiers par défaut. 
    
6. Ouvrez la vue concepteur de manifeste (par exemple, double-cliquez sur le fichier AppManifest.xml). Sous l’onglet **Général** , la zone de texte **titre** doit afficher le nom de l’application que vous avez tapé à l’étape 4. Choisissez l’onglet **autorisations** pour ajouter les demandes d’autorisation suivants pour l’application (voir Figure 2) : 
    
   - Dans la première ligne de la liste des **demandes d’autorisation** , dans la colonne **étendue** , sélectionnez **état** dans la liste déroulante. Dans la colonne **autorisation** , choisissez **SubmitStatus**.
    
   - Ajoutez une ligne où l' **étendue** est **Plusieurs projets** et l' **autorisation** **en lecture**.
    
   **La figure 2. Définition de l’étendue d’autorisation pour une application d’état**

   ![Définition de l’étendue d’autorisation pour une application d’état] (media/pj15_CreateStatusingApp_PermissionScope.gif "Définition de l’étendue d’autorisation pour une application d’état")
  
L’application **QuickStatus** permet à un utilisateur de Project Web App lire des affectations pour cet utilisateur à partir de plusieurs projets, modifier le pourcentage d’affectation et envoyer la mise à jour. Les autres étendues de demande autorisation indiquées dans la liste déroulante dans la Figure 2 ne sont pas nécessaires pour cette application. Les étendues des demandes d’autorisation sont les autorisations demandées par l’application au nom de l’utilisateur. Si l’utilisateur ne dispose pas des autorisations dans Project Web App, l’application ne s’exécute pas. Une application peut avoir plusieurs étendues des demandes d’autorisation, y compris celles des autres autorisations SharePoint, mais doit avoir le minimum nécessaire pour la fonctionnalité d’application. Voici les étendues des demandes d’autorisation associés à Project Server : 

- **Ressources d’entreprise**: autorisations de gestionnaire de ressources, pour lire ou écrire des informations sur les autres utilisateurs de Project Web App.
    
- **Plusieurs projets**: en lecture et en écriture à plusieurs projets, où l’utilisateur dispose des autorisations demandées.
    
- **Project Server**: oblige l’utilisateur de l’application d’avoir des autorisations d’administrateur pour Project Web App.
    
- **Création de rapports**: lire le service **ProjectData** OData pour Project Web App (requiert l’ouverture de session autorisation uniquement pour Project Web App). 
    
- **Projet unique**: en lecture et en écriture à un projet dans lequel l’utilisateur dispose des autorisations demandées.
    
- **État**: envoyer des mises à jour d’état des affectations, tels que des heures travaillées, pourcentage affectations complètes et nouveau.
    
- **Flux de travail**: si l’utilisateur est autorisé à exécuter des flux de travail Project Server, puis s’exécute l’application avec des autorisations élevées pour le flux de travail.
    
Pour plus d’informations sur les étendues des demandes d’autorisation pour Project Server 2013, consultez la section *applications Project* dans les [mises à jour pour les développeurs dans Project 2013](updates-for-developers-in-project-2013.md) et les [autorisations d’application dans SharePoint 2013](http://msdn.microsoft.com/library/fp142383.aspx).


<a name="pj15_StatusingApp_HTML"> </a>

### <a name="creating-the-html-content-for-the-quickstatus-app"></a>Création de contenu HTML pour l’application QuickStatus

Avant de commencer à coder le contenu HTML, concevez l’interface utilisateur et l’expérience utilisateur pour l’application QuickStatus (Figure 3 montre un exemple de la page terminé). Une conception peut également inclure un plan des fonctions JavaScript qui interagissent avec le code HTML. Pour plus d’informations, voir [conception de l’expérience utilisateur pour les applications dans SharePoint 2013](http://msdn.microsoft.com/library/fp179934.aspx).
  
**La figure 3. Conception de la page d’application QuickStatus**

![Conception de la page d’application QuickStatus] (media/pj15_CreateStatusingApp_AfterRefresh.gif "Conception de la page d’application QuickStatus")
  
L’application affiche le nom complet dans la partie supérieure, qui est la valeur de l’élément **Title** du fichier AppManifest.xml. 
  
Par défaut, la page utilise HTML5. Voici les éléments HTML standard pour les objets de l’interface utilisateur principales contenant l’application **QuickStatus** dans le corps de la page : 
  
- Un élément **form** contient tous les autres éléments de l’interface utilisateur. 
    
- Un élément de **jeu de champs** crée un conteneur et une bordure de la table des affectations ; l’élément de **légende** enfant fournit une étiquette pour le conteneur. 
    
- Un élément de **tableau** inclut une légende et un table en-tête. Fonctions JavaScript modifier la légende de table et ajouter des lignes pour les affectations. 
    
   > [!NOTE]
   > Pour ajouter facilement une pagination et un tri, une application de production utilisera probablement un contrôle commercial de grille basée sur jQuery plutôt qu’un tableau. 
  
   Le tableau inclut des colonnes pour le nom du projet, le nom de la tâche avec une case à cocher, le travail réel, le pourcentage de travail complète et autre, et date de fin de l’affectation. Fonctions JavaScript créent la case à cocher et le champ d’entrée de texte pour le pourcentage de chaque tâche.
    
- Un élément **d’entrée** pour une zone de texte définit le pourcentage achevé pour toutes les affectations sélectionnées. 
    
- Un élément **button** envoie les modifications de statut. 
    
- Un élément de **bouton** actualise la page. 
    
- Un élément **button** quitte l’application et retourne à la page tâches dans Project Web App. 
    
Les éléments de texte en bas et la case sont dans des éléments **div** , de sorte que CSS peut gérer facilement la position et l’apparence des objets de l’interface utilisateur. Une fonction JavaScript ajoute un paragraphe au bas de la page qui contient les résultats de la réussite ou l’échec de la mise à jour d’état. 
  
### <a name="procedure-2-to-create-the-html-content"></a>Procédure 2. Pour créer du contenu HTML

1. Dans Visual Studio, ouvrez le fichier Default.aspx.
    
   Le fichier comprend deux éléments **: Contenu asp** : l’élément avec le `ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` attribut est ajouté au sein de l’en-tête de page et l’élément avec le `ContentPlaceHolderID="PlaceHolderMain"` attribut est placé dans l’élément **body** de page. 
    
2. Dans la `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">` de contrôle pour l’en-tête de page, ajoutez une référence au fichier PS.js sur l’ordinateur Project Server. Pour tester et déboguer, vous pouvez utiliser PS.debug.js. 
    
   ```HTML
     <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
   ```

   L’infrastructure d’application utilise le `/_layouts/15/` un répertoire virtuel pour le site SharePoint dans IIS. Le fichier physique est `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.debug.js`.
    
   > [!NOTE]
   > Avant de déployer l’application pour la production, supprimer `.debug` dans les références de script pour améliorer les performances. 
  
3. Dans la `<asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">` de contrôle pour le corps de la page, supprimer l’élément généré **div** et ajoutez le code HTML pour les objets de l’interface utilisateur. L’élément de **tableau** contient une ligne d’en-tête. La colonne **nom de la tâche** inclut un contrôle d’entrée de case à cocher. Texte de l’élément de **légende** est remplacé par le rappel **onGetUserNameSuccess** pour la fonction **getUserInfo** dans le fichier App.js. 
    
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

4. Dans le fichier App.css, ajoutez le code CSS pour la position et l’apparence des éléments d’interface utilisateur. Pour le code CSS complet de l’application **QuickStatus** , consultez la section [exemple de code pour l’application QuickStatus](#pj15_StatusingApp_Example) . 
    
Procédure 3 ajoute les fonctions JavaScript pour lire les affectations et créer des lignes du tableau et pour modifier et mettre à jour le pourcentage d’affectation. Les étapes sont plus itératifs dans le développement d’une application, où vous pouvez également créer le code HTML, ajouter et tester les styles et les fonctions JavaScript, modifier ou ajouter davantage de code HTML, puis répétez le processus.

<a name="pj15_StatusingApp_JavaScript"> </a>

### <a name="creating-the-javascript-functions-for-the-quickstatus-app"></a>Création des fonctions JavaScript pour l’application QuickStatus

Le modèle Visual Studio pour une application SharePoint inclut le fichier App.js fichier, qui contient le code d’initialisation par défaut qui obtient le contexte de client SharePoint et illustre base obtenir et définir les actions de la page d’application. L’espace de noms JavaScript pour la bibliothèque de SP.js côté client SharePoint est **SP**. Comme une application Project Server utilise la bibliothèque PS.js, l’application utilise l’espace de noms **PS** pour obtenir le contexte client et accéder à la JSOM pour Project Server. 
  
Fonctions JavaScript dans l’application **QuickStatus** sont les suivantes : 
  
- Le Gestionnaire d’événements de document **prêt** s’exécute lorsque le modèle objet de document (DOM) est instancié. Le Gestionnaire d’événements **prêt** effectue les quatre étapes suivantes : 
    
    1. Initialise la variable globale **projContext** avec le contexte client pour le JSOM de serveur de projet et la variable globale **pwaWeb** . 
        
    2. Appelle la fonction **getUserInfo** pour initialiser la variable globale **projUser** . 
        
    3. Appelle la fonction **getAssignments** , qui obtient spécifié les données d’affectation de l’utilisateur. 
        
    4. Lie cliquez sur gestionnaires d’événements dans l’en-tête une table et les cases à cocher de chaque ligne du tableau. Les gestionnaires d’événements click gérer l’attribut **activé** les cases à cocher lorsque l’utilisateur sélectionne ou efface une case à cocher dans la table. 
    
- Si la fonction **getAssignments** se déroule correctement, il appelle la fonction **onGetAssignmentsSuccess** . Que fonction insère une ligne dans la table pour chaque affectation, initialise les contrôles HTML dans chaque ligne, puis initialise les propriétés du bouton bas. 
    
- Le Gestionnaire d’événements **onClick** pour le bouton de **mise à jour** appelle la fonction **updateAssignments** . Que fonction obtient la valeur de pourcentage achevé qui est appliquée à chaque affectation sélectionnée ; ou, si la zone de texte complète pour cent est vide, la fonction obtient le pourcentage complète de chaque affectation sélectionnée dans le tableau. La fonction **updateAssignments** puis enregistre et envoie les mises à jour d’état et écrit un message sur les résultats vers le bas de la page. 
    
### <a name="procedure-3-to-create-the-javascript-functions"></a>Procédure 3. Pour créer les fonctions JavaScript

1. Dans Visual Studio, ouvrez le fichier App.js, puis supprimez tout le contenu du fichier.
    
2. Ajoutez les variables globales et le Gestionnaire d’événements de document **prêt** . L’objet **document** est accessible à l’aide d’une fonction jQuery. 
    
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

3. Ajoutez la fonction **getUserInfo** , qui appelle **onGetUserNameSuccess** si la requête est réussie. La fonction **onGetUserNameSuccess** remplace le contenu du paragraphe **légende** avec une légende de table qui inclut le nom d’utilisateur. 
    
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

4. Ajoutez la fonction **getAssignments** , qui appelle **onGetAssignmentsSuccess** (voir l’étape 5) si la requête affectation se déroule correctement. L’option **inclure** la limite de la requête pour retourner uniquement les champs spécifiés. 
    
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

5. Ajoutez la fonction **onGetAssignmentsSuccess** , qui ajoute une ligne pour chaque affectation à la table. La variable **prevProjName** est utilisée pour déterminer si une ligne correspond à un autre projet. Dans ce cas, le nom du projet est affiché dans une police en gras ; Si ce n’est pas le cas, le nom du projet est défini sur une chaîne vide. 
    
   > [!NOTE]
   > Le JSOM n’inclut pas les propriétés **TimeSpan** qui inclut le modèle CSOM, tel que **ActualWorkTimeSpan**. Au lieu de cela, le JSOM utilise les propriétés pour le nombre de millisecondes, telles que la [PM. StatusAssignment.actualWorkMilliseconds](http://msdn.microsoft.com/library/736bce1e-f734-0efe-6c5f-e0e891ab00ef%28Office.15%29.aspx) propriété. La méthode pour obtenir cette propriété est **obtenir\_actualWorkMilliseconds**, qui retourne une valeur entière. > La méthode **get_actualWork** renvoie une chaîne, tel que « 3 h ». Vous pouvez utiliser des valeurs dans l’application **QuickStatus** , mais afficher différemment. La requête d’affectations inclut les deux propriétés, afin de tester la valeur lors du débogage. Si vous supprimez la variable **actualWork** , vous pouvez également supprimer la propriété **ActualWork** dans la requête d’affectations. 
  
   Enfin, la fonction **onGetAssignmentsSuccess** initialise le bouton **mise à jour** et le bouton **Actualiser** avec des gestionnaires d’événements click. La valeur de texte du bouton **mise à jour** peut également être définie dans le code HTML. 
    
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

6. Ajouter l' **updateAssignments** cliquez sur Gestionnaire d’événements pour le bouton de **mise à jour** . Lorsque l’utilisateur modifie une valeur de pourcentage d’achèvement d’une tâche ou ajoute une valeur dans la zone de texte **percentComplete** , la valeur peut être saisie dans plusieurs formats tels que « 60 », « 60 % » ou « 60 % ». La méthode **getNumericValue** renvoie la valeur numérique de la saisie de texte. 
    
   > [!NOTE]
   > Dans une application conçue pour une utilisation en production, les valeurs d’entrée pour les informations numériques doivent inclure une validation de champ et une vérification des erreurs supplémentaires. 
  
   L’exemple **updateAssignments** inclut une vérification des erreurs de base et affiche les informations dans le paragraphe **message** au bas de la page — vert si la requête de mise à jour est terminée et rouge s’il existe une erreur d’entrée ou la requête de mise à jour est Échec. 
    
   Avant d’utiliser la méthode **submitAllStatusUpdates** , l’application doit enregistrer les mises à jour sur le serveur à l’aide de la **PM. StatusAssignmentCollection.update** méthode. 
    
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

7. Ajoutez la fonction **exitToPwa** , qui utilise le paramètre de chaîne de requête **SPHostUrl** pour l’URL du site Project Web App hôte. Pour revenir à la page tâches, append `"/Tasks.aspx"` à l’URL. Par exemple, la variable **spHostUrl** est définie `https://ServerName/ProjectServerName/Tasks.aspx`.
    
   La fonction **getQueryStringParameter** fractionne l’URL de la page **QuickStatus** pour extraire et renvoyer le paramètre spécifié dans les options d’URL. Voici un exemple du document **. URL** valeur pour le document **QuickStatus** (tout sur une seule ligne) : 
    
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

   Pour l’ancienne URL, la fonction **getQueryStringParameter** renvoie la valeur de chaîne de requête **SPHostUrl** , `https://ServerName/pwa`. 
    
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

Si vous publiez l’application **QuickStatus** à ce stade et l’ajoutez à Project Web App, l’application peut être exécutée à partir de la page contenu du Site, mais il n’est pas facilement accessible aux utilisateurs. Pour aider les utilisateurs à trouver et exécuter l’application, vous pouvez ajouter un bouton pour qu’il au ruban dans la page tâches. Procédure 4 montre comment ajouter une action personnalisée du ruban. 

<a name="pj15_StatusingApp_ribbon"> </a>

### <a name="adding-a-ribbon-custom-action"></a>Ajout d’une action personnalisée du ruban

Onglets du ruban, groupes et contrôles pour Project Web App sont spécifiés dans le fichier pwaribbon.xml, qui est installé dans le `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\PWARibbon\listtemplates` répertoire sur l’ordinateur qui exécute Project Server. Pour faciliter la conception des actions personnalisées pour le ruban Project Web App, le téléchargement du Kit de développement Project 2013 inclut une copie de pwaribbon.xml. 
  
Project Web App utilise les définitions de ruban différent pour la page tâches, selon que l’instance Project Web App utilise le mode d’entrée unique qui permet aux utilisateurs d’entrer des valeurs pour l’état des tâches et feuilles de temps. Si vous disposez des autorisations d’administration pour Project Web App, pour déterminer le mode de saisie, choisissez **Paramètres PWA** dans le menu Paramètres de la liste déroulante en haut à droite de la page. Dans la page Paramètres de PWA, cliquez sur **paramètres de la feuille de temps et les valeurs par défaut**, puis examinez la case à cocher **Mode d’entrée unique** en bas de la page. 
  
Lorsque le mode d’entrée unique est désactivée, le ruban dans la page tâches est défini par la zone mon travail dans pwaribbon.xml : 
  
```XML
   <!-- REGION My Work Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.MyWork"
      . . .
```

Lorsque le mode d’entrée unique est activé, le ruban de la page tâches est défini par la région de Mode de lié dans pwaribbon.xml : 
  
```XML
   <!-- REGION Tied Mode Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.TiedMode"
      . . .
```

Bien que les groupes et des contrôles dans chaque région ressemble, un contrôle pour le mode de lié peut appeler une fonction autre que le même contrôle pour le mode non lié. Procédure 4 montre comment ajouter un contrôle de bouton pour l’application **QuickStatus** lorsque le mode d’entrée unique est désactivée (la case à cocher **Mode d’entrée unique** est désactivée). 
  
> [!NOTE]
> Pour obtenir des informations générales sur l’ajout d’actions personnalisées à un ruban ou à un menu dans une application SharePoint, voir [créer des actions personnalisées à déployer avec les applications pour SharePoint](http://msdn.microsoft.com/en-us/library/jj163954.aspx). 
  
### <a name="procedure-4-to-add-a-ribbon-custom-action-to-the-tasks-page"></a>Procédure 4. Pour ajouter une action personnalisée de ruban sur la page Tâches

1. Examinez le ruban dans la page tâches dans Project Web App. Sélectionnez l’onglet **tâches** dans le ruban et planifier comment la modifier. Il existe sept groupes, telles que **l’envoi**, **tâches**et **une période**. Le groupe **d’envoi** a deux contrôles, un bouton **Enregistrer** et un menu déroulant de **Envoyer l’état** . Vous pouvez ajouter un contrôle à n’importe quel emplacement dans un groupe, ajouter un groupe avec un nouveau contrôle à n’importe où dans l’onglet **tâches** ou ajouter un autre onglet du ruban qui a des contrôles et des groupes personnalisés. Dans cet exemple, nous ajouter un bouton tiers pour le groupe **d’envoi** , où le bouton appelle l’URL de l’application **QuickStatus** . 
    
2. Dans le volet de **L’Explorateur de solutions** dans Visual Studio, avec le bouton droit le projet **QuickStatus** , puis ajoutez un nouvel élément. Dans la boîte de dialogue **Ajouter un nouvel élément** , choisissez **Action personnalisée de ruban** (voir la Figure 4). Par exemple, nom de l’action personnalisée RibbonQuickStatusAction, puis choisissez **Ajouter**.
    
   **La figure 4. Ajout d’une action personnalisée du ruban**

   ![Ajout d’une action personnalisée du ruban] (media/pj15_CreateStatusingApp_AddRibbonCustomAction.gif "Ajout d’une action personnalisée du ruban")
  
3. Sur la première page de l’Assistant **Créer une Action personnalisée de ruban** , laissez l’option de **Site Web hôte** sélectionnée, choisissez **Aucun** dans la liste déroulante de l’étendue de l’action personnalisée, puis cliquez sur **suivant** (voir Figure 5). Les éléments dans les listes déroulantes sont pertinents pour SharePoint, pas à Project Server. Nous remplacera la plupart du code XML généré pour l’action personnalisée afin qu’elle s’applique à Project Server. 
    
   **La figure 5. Spécification des propriétés de l’action personnalisée du ruban**

   ![Spécification des propriétés de l’action personnalisée du ruban] (media/pj15_CreateStatusingApp_RibbonCustomAction2.gif "Spécification des propriétés de l’action personnalisée du ruban")
  
4. Dans la page suivante de l’Assistant **Créer une Action personnalisée de ruban** , laissez toutes les valeurs par défaut pour les paramètres, puis cliquez sur **Terminer** (voir Figure 6). Visual Studio crée le dossier **RibbonQuickStatusAction** , qui contient un fichier Elements.xml. 
    
   **La figure 6. Définition des paramètres pour un contrôle de bouton**

   ![Définition des paramètres pour un contrôle de bouton] (media/pj15_CreateStatusingApp_RibbonCustomAction3.gif "Définition des paramètres pour un contrôle de bouton")
  
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

   1. Dans l’élément **CustomAction** , supprimez l’attribut **Sequence** et l’attribut **Title** . 
    
   2. Pour ajouter un contrôle pour le groupe **d’envoi** , recherchez le premier groupe dans le `Ribbon.ContextualTabs.MyWork.Home.Groups` collection dans le fichier pwaribbon.xml, qui est l’élément qui commence, `<Group Id="Ribbon.ContextualTabs.MyWork.Home.Page" Command="PageGroup" Sequence="10" Title="$Resources:pwafeatures,PAGE_PDP_CM_SUBMIT"`. Pour ajouter un contrôle enfant pour le groupe **Envoyer** , le code suivant illustre l’attribut **Location** correct de l’élément **CommandUIDefinition** dans le fichier Elements.xml : 
    
      ```XML
        <CommandUIDefinitions>
          <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
             . . .
          </CommandUIDefinition>
        </CommandUIDefinitions>
      ```

   3. Modifier les valeurs d’attribut de l’élément de **bouton** enfant comme suit : 
    
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

       - Pour rendre le bouton de la troisième contrôle dans le groupe, l’attribut **Sequence** peut être n’importe quel nombre supérieur à la `Sequence="20"` valeur du contrôle **Envoyer l’état** existant (qui est un élément **FlyoutAnchor** dans pwaribbon.xml). Par convention, les numéros de séquence des groupes et des contrôles sont `10, 20, 30, …`, ce qui permet d’éléments à insérer dans les positions intermédiaires.
    
       - L’attribut de **commande** spécifie la commande à exécuter dans l’élément **CommandUIHandler** (voir l’étape 5.d). Vous pouvez simplifier le nom de la commande pour le rendre plus facile pour les développeurs suivant. Par exemple `Command="Invoke_QuickStatus"` est plus facile à lire que `Command="Invoke_RibbonQuickStatusActionButtonRequest"`.
    
       - Les attributs d’image spécifient l’icône de 16 x 16 pixels et l’icône de 32 x 32 pixels pour le contrôle bouton. Dans le fichier Elements.xml par défaut, `Image32by32="_layouts/15/images/placeholder32x32.png"` spécifie un point orange. Vous pouvez extraire des icônes dans les fichiers de mappage d’image (ps16x16.png et ps32x32.png) qui sont installés dans le `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\1033\IMAGES` répertoire sur l’ordinateur qui exécute Project Server. Par exemple, l’icône de 32 x 32 pixels est dans la deuxième colonne des icônes à partir de la gauche et la dixième ligne vers le bas à partir du haut de l’image interactive ps32x32.png (la partie supérieure de l’icône est postérieure à la fin de la neuvième ligne ; 9 x 32 pixels/lignes = 288 pixels). 
    
       - Pour afficher une info-bulle pour le contrôle bouton, ajoutez les attributs **ToolTipTitle** et **ToolTipDescription** . 
    
    4. Modifier les attributs de l’élément **CommandUIHandler** . Par exemple, assurez-vous que l’attribut de **commande** correspond à la valeur d’attribut pour l’élément de **bouton de** **commande** . Pour l’attribut **commandaction code** , `~appWebUrl` est un espace réservé pour l’URL de la page Web **QuickStatus** . Lorsque le bouton de ruban appelle l’application **QuickStatus** , le jeton **{StandardTokens}** est remplacé par options d’URL qui incluent **SPHostUrl**, **SPLanguage**, **SPClientTag**, **SPProductNumber**et **SPAppWebUrl **.
    
        ```XML
            <CommandUIHandlers>
                <CommandUIHandler Command="Invoke_QuickStatus"
                                  CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
            </CommandUIHandlers>
        ```

6. Dans **L’Explorateur de solutions**, ouvrez le concepteur **Feature1.feature** et déplacer l’élément **RibbonQuickStatusAction** dans le volet **éléments de la Solution** dans le volet **éléments de la fonctionnalité** . Si vous ouvrez le concepteur **Package.package** , l’élément **RibbonQuickStatusAction** sera dans le volet **éléments dans le Package** . 
    
Lorsque vous développez l’application et ajoutez un bouton de ruban, normalement tester l’application et définir des points d’arrêt dans le code JavaScript pour le débogage. Lorsque vous appuyez sur **F5** pour démarrer le débogage, Visual Studio compile l’application, le déploie sur le site qui est spécifié dans la propriété **URL du Site** du projet **QuickStatus** et affiche une page qui vous demande si vous faites confiance à l’application. Lorsque vous passez, puis quittez l’application **QuickStatus** , il renvoie à la page tâches dans Project Web App. 

> [!NOTE]
> La figure 7 montre que le bouton **Statut rapide** sur l’onglet **tâches** du ruban est désactivé. Une fois les nombreuses déboguer des déploiements avec Visual Studio, les contrôles de ruban personnalisé peuvent être bloquées lorsque vous continuez à déboguer ou déployer l’application publiée sur le même serveur de test. Pour activer le bouton, supprimer l’élément **RibbonQuickStatusAction** dans Visual Studio et puis créer une nouvelle action de ruban qui a un autre nom et ID. Si cela ne résout pas le problème, essayez de supprimer l’application de l’instance de test de Project Web App, puis recréer l’application avec un ID d’application différents. 
  
**La figure 7. Affichage de l’info-bulle du bouton rapide de l’état désactivé**

![Affichage de l’info-bulle du bouton désactivé] (media/pj15_CreateStatusingApp_ButtonToolTipDisabled.gif "Affichage de l’info-bulle du bouton désactivé")
  
Procédure 5 montre comment déployer et installer l’application **QuickStatus** . Procédure 6 indique des étapes supplémentaires dans les tests de l’application une fois que vous l’avez installé. 

<a name="pj15_StatusingApp_Deploying"> </a>

## <a name="deploying-the-quickstatus-app"></a>Déploiement de l’application QuickStatus

Il existe plusieurs manières de déployer une application à une application web de SharePoint, comme Project Web App. Le déploiement que vous utilisez dépend de si vous souhaitez publier l’application à un catalogue privé de SharePoint ou à l’Office Store public, et si SharePoint est installé sur site ou une architecture en ligne. Procédure 5 montre comment déployer l’application **QuickStatus** à une installation locale dans un catalogue d’applications privé. Pour plus d’informations, voir [installer et gérer des applications pour SharePoint 2013](http://technet.microsoft.com/library/fp161232.aspx) et [publier des applications pour SharePoint](http://msdn.microsoft.com/library/jj164070.aspx)
  
> [!NOTE]
> L’ajout d’une application à un catalogue SharePoint nécessite des autorisations d’administrateur SharePoint. 
  
### <a name="procedure-5-to-deploy-the-quickstatus-app"></a>Procédure 5. Pour déployer l’application QuickStatus

1. Dans Visual Studio, enregistrez tous les fichiers, puis cliquez sur le projet **QuickStatus** dans l' **Explorateur de solutions** et choisissez **Publier**.
    
2. Étant donné que l’application **QuickStatus** est hébergée sur SharePoint, il existe très peu d’options pour la publication (voir Figure 8). Dans la boîte de dialogue **publier des applications pour Office et SharePoint** , cliquez sur **Terminer**.
    
   **La figure 8. Publication de l’application QuickStatus**

   ![à l’aide de l’Assistant Publication] (media/pj15_CreateStatusingApp_PublishWizard.gif "à l’aide de l’Assistant Publication")
  
3. Copiez le fichier QuickStatus.app à partir de la `~\QuickStatus\bin\Debug\app.publish\1.0.0.0` répertoire vers un répertoire approprié sur l’ordinateur local (ou sur l’ordinateur SharePoint pour une installation sur site). 
    
4. Dans l’Administration centrale SharePoint, choisissez **applications** dans la barre de lancement rapide, puis cliquez sur **Gérer le catalogue d’applications**.
    
5. Si un catalogue d’applications n’existe pas, créez une collection de sites pour le catalogue d’applications, en suivant la section *configurer le site de catalogue d’applications pour une application web* dans [gérer le catalogue d’applications dans SharePoint 2013](http://technet.microsoft.com/library/fp161234.aspx).
    
   Si un catalogue d’applications existe, accédez à l’URL du site dans la page Gérer le catalogue application. Par exemple, dans les étapes suivantes, le site de catalogue d’applications est `http://ServerName/sites/TestApps`.
    
6. Dans la page catalogue application, choisissez **applications pour SharePoint** dans la barre de lancement rapide. Dans les page applications pour SharePoint, sous l’onglet **fichiers** du ruban, cliquez sur **Télécharger un Document**.
    
7. Dans la boîte de dialogue **Ajouter un document** , recherchez le fichier QuickStatus.app, ajouter des commentaires de la version, puis cliquez sur **OK**.
    
8. Lorsque vous ajoutez une application, vous pouvez également ajouter des informations locales pour la description de l’application, d’icône et d’autres informations. Dans la boîte de dialogue **applications pour SharePoint - QuickStatus.app** , ajoutez les informations que vous souhaitez afficher pour l’application dans la collection de sites SharePoint. Par exemple, ajoutez les informations suivantes : 
    
   1. **Courte** Description : application de test de Type rapide de l’état.
    
   2. Champ de **Description** : application de Test de Type pour mettre à jour le pourcentage d’achèvement des tâches dans plusieurs projets.
    
   3. **URL de l’icône** champs : ajouter une image de 96 x 96 pixels pour l’icône d’application pour les éléments de site pour le catalogue d’applications. Par exemple, accédez à `http://ServerName/sites/TestApps`, choisissez **contenu du Site** dans le menu déroulant **paramètres** , choisissez **Éléments de Site**et ajoutez l’image quickStatusApp.png. Avec le bouton droit de l’élément **quickStatusApp** , choisissez **Propriétés**, puis copiez la valeur **Adresse (URL)** dans la boîte de dialogue **Propriétés** . Par exemple, copiez `http://ServerName/sites/TestApps/SiteAssets/QuickStatusApp.png`, puis collez la valeur dans le champ d’adresse **URL de l’icône** web. Tapez une description de l’icône, par exemple (comme illustré à la Figure 9), tapez l’icône de l’application QuickStatus. Vérifiez que l’URL est valide.
    
      **La figure 9. Ajout d’une URL de l’icône de l’application QuickStatus**

      ![Définition des propriétés dans SharePoint pour l’application] (media/pj15_CreateStatusingApp_AddAppToSharePointSettings.gif "Définition des propriétés dans SharePoint pour l’application")
  
   4. Champ de **catégorie** : choisir une catégorie existante ou spécifier votre propre valeur. Par exemple, tapez état.
    
      > [!NOTE]
      > Une catégorie nommée **état** est uniquement à des fins de test. Une catégorie par défaut pour les applications de Project Server est la **Gestion de projet**. 
  
   5. Champ **nom de l’éditeur** : tapez le nom de l’éditeur. Dans cet exemple, tapez SDK Project.
    
   6. Champ **activé** : pour rendre l’application visible pour les administrateurs de site Project Web App pour l’installation, activez **la case à cocher** . 
    
   7. Des champs supplémentaires sont facultatives. Par exemple, vous pouvez ajouter une URL de prise en charge et de plusieurs images d’aide pour la page Détails de l’application. Dans la Figure 9, les champs **d’Image URL 1** incluent l’URL pour une capture d’écran de l’application et une description de la capture d’écran. 
    
   8. Dans la boîte de dialogue **applications pour SharePoint - QuickStatus.app** , cliquez sur **Enregistrer**. Dans la Figure 9, l’élément de **Mise à jour de statut rapide** dans les applications de bibliothèque SharePoint est extrait pour modification, etc. l’onglet **Modifier** du ruban de boîte de dialogue, choisissez **Archiver** pour terminer le processus (voir Figure 10). 
    
      **La figure 10. L’application QuickStatus est ajoutée pour les applications de bibliothèque SharePoint.**

      ![Application du QuickStatus est ajoutée à SharePoint] (media/pj15_CreateStatusingApp_AddAppToSharePoint.gif "Application du QuickStatus est ajoutée à SharePoint")
  
9. Dans Project Web App, dans le menu déroulant **paramètres** , choisissez **Ajouter une application**. Dans la page de vos applications, dans la barre de lancement rapide, choisissez **De votre organisation**, puis cliquez sur **Détails de l’application** pour l’application de **Mise à jour de statut rapide** . La figure 11 montre la page de détails avec l’icône d’application, capture d’écran et d’autres informations que vous avez ajouté à l’étape précédente. 
    
   **La figure 11. À l’aide de la page de détails de mise à jour de statut rapide dans Project Web App**

   ![Ajout de l’application QuickStatus à Project Web App] (media/pj15_CreateStatusingApp_AddAppToPWA.gif "Ajout de l’application QuickStatus à Project Web App")
  
10. Dans la page Détails de la mise à jour de statut rapide, sélectionnez **Ajouter**. Project Web App affiche une boîte de dialogue qui répertorie les opérations que l’application QuickStatus peut effectuer (voir Figure 12). La liste des opérations est dérivée à partir des éléments **AppPermissionRequest** dans le fichier AppManifest.xml. 
    
    **La figure 12. Vérification que vous faites confiance à l’application rapide de l’état**

    ![Vérification de l’approbation pour l’application QuickStatus] (media/pj15_CreateStatusingApp_AddAppToPWA2Trust.gif "Vérification de l’approbation pour l’application QuickStatus")
  
11. Dans la boîte de dialogue **approuvez-vous rapide mise à jour d’état** , sélectionnez **Gestion de la confidentialité**. L’application est ajoutée à la page contenu du Site Project Web App (voir la Figure 13).
    
    **La figure 13. Affichage de l’application rapide de l’état dans la page contenu du Site**

    ![Affichage de l’application QuickStatus dans le contenu du Site] (media/pj15_CreateStatusingApp_AddAppToPWA3.gif "Affichage de l’application QuickStatus dans le contenu du Site")
  
Dans la page contenu du Site, vous pouvez sélectionner l’icône de **Mise à jour de statut rapide** pour exécuter l’application.

> [!NOTE]
> Pour les commandes supplémentaires qui fournissent des informations sur l’application, dans la page contenu du Site, choisissez la région contenant le nom de la **Mise à jour de statut rapide** et les points de suspension (...). Vous pouvez consulter la page à propos de l’application, afficher la page Détails de l’application qui contient des informations sur les erreurs d’application, passez en revue la page autorisations de l’application ou supprimer l’application à partir de Project Web App. 
  
Dans la page tâches dans Project Web App (voir Figure 14), le bouton **QuickStatus** doit être activé sur le ruban. Si le bouton **Rapide de l’état** est désactivé, essayez les actions décrites dans la note de la Figure 7. 

**La figure 14. Démarrage de l’application QuickStatus à partir de l’onglet tâches**

![Démarrage de l’application QuickStatus à partir de l’onglet tâches] (media/pj15_CreateStatusingApp_TasksRibbon.gif "Démarrage de l’application QuickStatus à partir de l’onglet tâches")
  
La procédure 6 décrit certains tests à effectuer avec l’application QuickStatus.

<a name="pj15_StatusingApp_Testing"> </a>

## <a name="testing-the-quickstatus-app"></a>Test de l’application QuickStatus

Chaque opération un utilisateur peut essayer dans l’application **QuickStatus** doit être testée sur une installation de test de Project Server avant de déployer l’application sur un serveur de production ou à un client de production de Project Online. Une installation de test vous permet de modifier et supprimer des affectations pour les utilisateurs sans affecter les projets réels. Le test doit également implique plusieurs utilisateurs qui disposent de plusieurs ensembles d’autorisations, comme administrateur, responsable de projet et membre d’équipe. Test complet peut révéler des modifications doivent être effectuées dans l’application, qui n’ont pas étaient apparentes de test lors du développement. Procédure 6 répertorie plusieurs tests pour l’application **QuickStatus** , mais n’inclut pas une série de tests exhaustive. 
  
### <a name="procedure-6-to-test-the-quickstatus-app"></a>Procédure 6. Pour tester l’application QuickStatus

1. Exécutez l’application **QuickStatus** dans lequel l’utilisateur n’a aucune affectation. L’application doit afficher un message au bas de la page, par exemple, **nom d’utilisateur ne comporte aucune affectation de**bleu.
    
   Choisissez la **mise à jour**et les modifications de message à un vert **affectations ont été mis à jour**.
    
   > [!NOTE]
   > Le comportement de l’application doit être modifié afin que la **mise à jour** est désactivé quand il n’y a aucune affectation. 
  
2. Exécutez l’application dans laquelle l’utilisateur a plusieurs affectations dans plusieurs projets différents et pour laquelle certaines affectations ne sont pas terminées. Notez l’apparence de l’application et effectuez les actions suivantes (voir la figure 15) :
    
   1. La fonction **onGetAssignmentsSuccess** crée une ligne dans la table pour chaque affectation pour l’utilisateur actuel. Le nom du projet ne montre qu’une seule fois, dans une police en gras, pour la première affectation dans chaque projet. 
    
   2. Désactivez la case à cocher dans l’en-tête de colonne **nom de la tâche** . L’en-tête du tableau cliquez sur efface de gestionnaire d’événements toutes l’autres à cocher cases dans les lignes tâche. 
    
   3. Sélectionnez toutes les tâches. Le Gestionnaire d’événements click pour chaque ligne détermine si toutes les lignes sont sélectionnées et le cas échéant, sélectionne l’en-tête de colonne **nom de la tâche** . 
    
   4. Désactivez toutes les cases à cocher à nouveau, puis sélectionnez une affectation avec un travail restant. Par exemple, la figure 15 montre que la tâche supérieure T1 a 20 % de travail restant à terminer.
    
   5. Dans la zone de texte **définir le pourcentage achevé** , tapez 80, puis cliquez sur **mise à jour**. La partie inférieure de la page doit afficher un message vert, **affectations ont été mis à jour**.
    
      **La figure 15. Mise à jour d’une affectation dans l’application QuickStatus**

      ![Mise à jour d’une affectation dans l’application QuickStatus] (media/pj15_CreateStatusingApp_Testing1Update.gif "Mise à jour d’une affectation dans l’application QuickStatus")
  
3. Choisissez **Actualiser** (voir Figure 16). Toutes les tâches sont à nouveau sélectionnés et les tâches principales montre 80 % terminée. 
    
      **La figure 16. Actualiser la page mise à jour de statut rapide**

      ![Actualiser la page QuickStatus] (media/pj15_CreateStatusingApp_Testing2Refresh.gif "Actualiser la page QuickStatus")
  
4. Désactivez toutes les cases à cocher, puis sélectionnez une autre tâche. Par exemple, sélectionnez **nouvelle tâche dans PWA**. Renseignez la zone de texte **définir le pourcentage achevé** , supprimez tout le texte dans la colonne de **pourcentage d’achèvement** de la tâche sélectionnée, puis cliquez sur **mise à jour**. Étant donné que les deux zones de texte sont vides, l’application affiche une erreur rouge (voir Figure 17) du message.
    
      **La figure 17. Tester le message d’erreur**

      ![Tester le message d’erreur] (media/pj15_CreateStatusingApp_Testing3Error.gif "Tester le message d’erreur")
  
5. Mettre à jour de la tâche précédente à 80 %, puis sur **Quitter**. La fonction **exitToPwa** modifie l’emplacement de fenêtre de navigateur à la page tâches dans l’application hôte SharePoint (autrement dit, l’URL devient https://ServerName/pwa/Tasks.aspx). La figure 18 montre que la tâche **T1** et la tâche de la **nouvelle tâche dans PWA** affichent 80 % terminée. 
    
      **La figure 18. Vérification des tâches sont mises à jour dans Project Web App**

      ![Vérification des tâches mis à jour dans Project Web App] (media/pj15_CreateStatusingApp_TasksUpdatedInPWA.gif "Vérification des tâches mis à jour dans Project Web App")
  
6. Avant la mise à jour d’état affiche dans Project Professional 2013, les modifications doivent être soumises à approbation et approuvées par le responsable de projet.
    
Test révèle plusieurs autres modifications doivent être effectuées dans l’application **QuickStatus** pour l’amélioration de la convivialité. Par exemple :

- Il doit être vérifications des erreurs supplémentaires et validation des valeurs de zone de texte. Actuellement, un utilisateur peut entrer une valeur non numérique ou une valeur négative pour cent, ce qui se traduit par un message d’erreur hostiles. Par exemple, avec une valeur négative, le message d’erreur est **erreur mise à jour d’affectations : PJClientCallableException : StatusingSetDataValueInvalid**.
    
- Le message d’erreur pour les zones de texte vides peut indiquer le projet et la tâche, en plus du numéro de ligne.
    
- Le message de réussite peut inclure une liste des tâches de mise à jour ; ou, si la fonction **updateAssignments** se déroule correctement, il peut effectuer une actualisation automatique des pages et afficher les tâches mises à jour ou pourcentages dans une couleur différente et une police en gras. 
    
- Pour éviter un tableau très volumineux, le tableau des affectations doit être limité aux tâches inférieures à 100 % de travail achevé. Sinon, ajoutez une option pour afficher toutes les tâches. Ce problème peut également être résolu à l’aide d’une grille basée sur jQuery plutôt que sur un tableau, où vous pouvez facilement implémenter le filtrage et la grille de pagination.
    
- Étant donné que l’application **QuickStatus** ne présente pas d’état, l’icône de **Statut rapide** sur l’onglet **tâches** du ruban serait plus logiquement la première icône dans le groupe **tâches** , plutôt que la dernière icône dans le groupe **d’envoi** . 
    
- Étant donné que la fonction **onGetAssignmentsSuccess** initialise le texte du bouton **btnSubmitUpdate** , mais les autres valeurs de texte de bouton sont initialisés dans le code HTML, la page reste dans un état partiellement initialisé lors de la **getAssignments** la fonction s’exécute. Boutons de la page apparaissent plus cohérents si les valeurs de texte ont été initialisés dans le code HTML. 
    
Plus important, l’approche de l’application **QuickStatus** utilise, où il transforme en pour cent effectuer pour des affectations, doit être révisé dans une application de production. Pour plus d’informations, voir la section [étapes suivantes](#pj15_StatusingApp_NextSteps) . 

<a name="pj15_StatusingApp_Example"> </a>

## <a name="example-code-for-the-quickstatus-app"></a>Exemple de code pour l’application QuickStatus

### <a name="defaultaspx-file"></a>Fichier default.aspx

Le code suivant se trouve dans le `Pages\Default.aspx` fichier du projet **QuickStatus** : 
  
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

### <a name="appjs-file"></a>Fichier App.js

Le code suivant se trouve dans le `Scripts\App.js` fichier du projet **QuickStatus** : 
  
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

### <a name="appcss-file"></a>Fichier App.CSS

Le code CSS suivant se trouve dans le `Content\App.css` fichier du projet **QuickStatus** : 
  
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

### <a name="elementsxml-file-for-the-ribbon"></a>Fichier Elements.XML pour le ruban

La définition XML suivante, pour le bouton ajouté sous l’onglet **tâches** dans le ruban, est la `RibbonQuickStatusAction\Elements.xml` fichier du projet **QuickStatus** : 
  
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

### <a name="appmanifestxml-file"></a>Fichier AppManifest.xml

Voici le code XML pour le manifeste d’application du projet **QuickStatus** , qui inclut les deux étendues des demandes d’autorisation qui sont nécessaires pour mettre à jour d’état de l’affectation de l’utilisateur d’application dans plusieurs projets : 
  
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
        <AppPermissionRequest Scope="http://sharepoint/projectserver/statusing" Right="SubmitStatus" />
        <AppPermissionRequest Scope="http://sharepoint/projectserver/projects" Right="Read" />
    </AppPermissionRequests>
    </App>
```

<br/>

### <a name="appiconpng-file"></a>Fichier AppIcon.png

La solution Visual Studio complète pour l’application **QuickStatus** inclut un fichier AppIcon.png personnalisé. La solution sera incluse dans le téléchargement du Kit de développement Project 2013. 

<a name="pj15_StatusingApp_NextSteps"> </a>

## <a name="next-steps"></a>Étapes suivantes

L’application **QuickStatus** est un exemple simple de l’écriture d’applications qui peuvent être installées sur Project Server 2013 et Project Online. La section [test de l’application QuickStatus](#pj15_StatusingApp_Testing) répertorie plusieurs améliorations qui peuvent être effectuées pour une meilleure convivialité. L’application **QuickStatus** utilise les fonctions JavaScript pour mettre à jour d’état de l’affectation pour Project Web App. Mais, modifier le pourcentage d’affectation n’est pas une pratique de gestion de projet recommandés. Une autre approche consisterait à mettre à jour la date de début réelle et la durée restante des tâches affectées. Pour une description des problèmes, consultez [Une meilleure mise à jour](http://www.mpug.com/articles/update-better) dans le bulletin MPUG. 

<a name="pj15_StatusingApp_AdditionalResources"> </a>

## <a name="see-also"></a>Voir aussi

- [Tâches de programmation de Project Server](project-programming-tasks.md)
- [Compléments](http://msdn.microsoft.com/library/jj163230.aspx)
- [Gestion des mises à jour de tâches dans Project Web App](https://technet.microsoft.com/en-us/library/hh767481%28v=office.14%29.aspx)
- [Créer des actions personnalisées à déployer avec les compléments SharePoint](http://msdn.microsoft.com/library/jj163954.aspx)
    

