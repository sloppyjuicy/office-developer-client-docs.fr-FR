---
title: Créer un flux de travail Project Server pour la gestion de la demande
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: b0e4a3b3-d1df-454d-b74c-b980b0b456f6
description: Cet article explique comment créer un flux de travail simple à l’aide de SharePoint Designer 2013.
ms.openlocfilehash: bbefc5d30ccb508a24c32fe41e733e6e8187ecd9
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388300"
---
# <a name="create-a-project-server-workflow-for-demand-management"></a>Créer un flux de travail Project Server pour la gestion de la demande

Cet article explique comment créer un flux de travail simple à l’aide de SharePoint Designer 2013. Vous pouvez exporter le flux de travail dans Visio 2013 pour la visualisation et la modification, ou utiliser Visio 2013 pour les flux de travail Project Server 2013 de conception et importer la conception dans SharePoint Designer 2013 pour publication à Project Web App. Pour plus d’informations sur la plateforme de flux de travail SharePoint et création de flux de travail avec Visio 2013 et SharePoint Designer 2013, voir les articles de [flux de travail dans SharePoint 2013](https://msdn.microsoft.com/library/jj163986%28office.15%29.aspx) dans la documentation du développeur SharePoint 2013. 
  
Pour plus d’informations sur la préparation de Project Server de flux de travail, voir [Démarrer : définissez vers le haut et configurer le Gestionnaire de flux de travail SharePoint 2013](https://msdn.microsoft.com/library/jj163276%28office.15%29.aspx).

<a name="pj15_CreateWorkflowSPD_General"> </a>

## <a name="creating-a-general-workflow"></a>Création d’un flux de travail général

Utilisez les étapes suivantes pour créer un flux de travail Project Server 2013 à l’aide de SharePoint Designer 2013. Le flux de travail est conçu pour la gestion de la demande de propositions de projet.
  
Pour obtenir la procédure détaillée, voir la section [Création d’un flux de travail de branchement](#pj15_CreateWorkflowSPD_Detailed) . 
  
### <a name="to-create-a-project-server-workflow-general-procedure"></a>Pour créer un flux de travail Project Server (procédure générale)

1. Déterminez les conditions requises et concevez le flux de travail. Organisez-le par phases et par étapes, puis déterminez les champs personnalisés qu’il utilisera.
    
2. Dans Project Web App, créez les entités qui requiert le flux de travail :
    
    1. Passez en revue les phases de flux de travail existantes et créez-en d’autres si nécessaire.
        
    2. Créez les champs personnalisés d’entreprise que le flux de travail utilisera. Pour être disponible dans l’étape d’un flux de travail, un champ personnalisé doit être contrôlé par un flux de travail.
        
    3. Modifiez ou créez les pages de détails de projet (PDP) que les étapes de votre flux de travail utiliseront en vue de recueillir des informations pour le projet. Dans cet exemple, les étapes utilisent des PDP par défaut, modifiées pour inclure un nouveau champ personnalisé.
        
    4. Créez les étapes du flux de travail nécessaires, puis associez chacun d’elle à la phase appropriée.
    
3. Dans SharePoint Designer 2013, construisez le flux de travail à l’aide d’instructions déclaratives dans le **Concepteur texte**:
    
    > [!NOTE]
    > Vous pouvez également utiliser le **Concepteur visuel** dans SharePoint Designer 2013 ou importer un flux de travail existant à partir de Visio 2013. Procédez comme suit pour utiliser le **Concepteur texte**: 
    > 
    > 1. Ouvrez le site Project Web App, puis créer un flux de travail de site qui utilise la plateforme de flux de travail **SharePoint 2013 Workflow - Project Server** . 
    > 2. Ajoutez les étapes utilisées par le flux de travail.
    > 3. Insérez les étapes, les conditions, les actions et les boucles du flux de travail requises à chaque étape.
    > 4. Recherchez les éventuelles erreurs de flux de travail et corrigez-les si vous en détectez.
    > 5. (Facultatif) Basculer l’affichage vers le **Concepteur visuel**, ou exporter des flux de travail dans un fichier Visio 2013. Vous pouvez modifier l’affichage de Visio et enregistrer les modifications dans le flux de travail en cours. Vous pouvez modifier le fichier Visio et importez-le dans SharePoint Designer 2013 pour créer d’autres workflows.
    > 6. Publier le flux de travail. Une fois qu’il est publié, le flux de travail s’affiche dans la liste des flux de travail pour le site Project Web App.
    
4. Dans Project Web App, utilisez le flux de travail pour la gestion de la demande des propositions de projet :
    
    1. Créez un modèle de projet d’entreprise (EPT) qui utilise le flux de travail.
        
    2. Sur la page du centre de projets, créez un projet qui utilise l’EPT pour le flux de travail, puis suivez les étapes du flux de travail.
        
    3. Testez rigoureusement le flux de travail.
        
    4. Déployez le flux de travail sur un serveur de production.

<a name="pj15_CreateWorkflowSPD_Detailed"> </a>

## <a name="creating-a-branching-workflow"></a>Création d’un flux de travail de branchement

Avant de pouvoir utiliser SharePoint Designer 2013 pour créer un flux de travail Project Server, le service de Workflow Manager Client 1.0 doit être configuré pour utiliser les activités de flux de travail Project Server 2013. Pour plus d’informations sur la configuration du Workflow Manager Client 1.0, voir les articles de [flux de travail dans SharePoint 2013](https://msdn.microsoft.com/library/jj163986%28office.15%29.aspx) dans la documentation du développeur SharePoint Server 2013. 
  
La procédure détaillée ci-après comprend les mêmes étapes que la section [Création d’un flux de travail général](#pj15_CreateWorkflowSPD_General) . 
  
### <a name="to-create-a-project-server-branching-workflow-detailed-procedure"></a>Pour créer un flux de travail de branchement Project Server (procédure détaillée)

#### <a name="1-plan-and-design-the-workflow"></a>1. permet de planifier et concevoir le flux de travail.

Un flux de travail Project Server peut s’intégrer avec plusieurs étapes et phases dans un processus de gestion de la demande. Flux de travail pouvant être complexe, vous devez comprendre les besoins commerciaux et planifier un flux de travail avec soin. Pour obtenir un exemple simple, concevez un flux de travail de branchement qui utilise le coût estimé d’une proposition de projet afin de déterminer si la proposition est acceptée. Si le coût estimé est supérieur à 25 000 dollars, rejeter la proposition ; dans le cas contraire, accepter la proposition et créer le projet.
    
Étant donné que vous pouvez utiliser Visio 2013 et SharePoint Designer 2013 pour concevoir et créer des flux de travail pour Project Server 2013, vous pouvez tester plus facilement avec les flux de travail avec Project Server 2010. L’exemple de conception de flux de travail dans cet article est le même que dans l’article [créer un flux de travail de branchement](https://msdn.microsoft.com/library/a02cafdc-d881-4271-b446-d8b2cd456a52%28Office.15%29.aspx) dans le SDK Project 2010. Vous pouvez concevoir et créer un flux de travail de test sur un ordinateur distant à l’aide d’une instance de test de Project Web App, vous n’êtes pas obligé de créer des flux de travail directement sur un ordinateur de Project Server 2013. 
    
#### <a name="2-create-the-entities-that-your-workflow-requires"></a>2. Créez les entités qui requiert votre flux de travail.

Dans Project Web App, passez en revue les phases de flux de travail disponibles et les phases et les champs personnalisés d’entreprise disponibles. Si nécessaire, créez les entités qui nécessite votre flux de travail, comme dans les étapes suivantes :
    
1. **Phases du flux de travail** L’installation par défaut de Project Web App inclut le créer, sélectionner, planifier, gérer et phases terminées. L’exemple de flux de travail branchement, vous n’avez pas créer d’autres phases. 
        
2. **Champs personnalisés d’entreprise** Le flux de travail de branchement nécessite un champ personnalisé de coût projet qui est contrôlé par flux de travail. La valeur d’un champ personnalisé contrôlé par flux de travail est définie dans un PDP qui utilise le flux de travail. Par exemple, choisissez l’icône **paramètres** en haut à droite d’une page de Project Web App, choisissez **Paramètres de PWA**, puis cliquez sur **Tables de choix et champs personnalisés d’entreprise**.
        
   Créer un champ personnalisé nommé coût de la proposition pour l’entité du **projet** et sélectionnez le type de **coût**. Pour la description, tapez le coût estimé d’une proposition de projet. Dans la section **comportement** , sélectionnez **le comportement contrôlé par flux de travail**.
        
3. **Pages de détails de projet** Modifier ou créer les PDP qui utiliseront des étapes du flux de travail. Par exemple, procédez comme suit : 
        
    1. Sélectionnez **Pages de détails de projet** sur la page Paramètres du serveur, puis choisissez la PDP **Informations sur le projet**. 
            
    2. Sur l’onglet **PAGE** du ruban, dans le groupe **Modifier**, choisissez **Modifier la page**.
            
    3. Cliquez sur la flèche du bas dans le coin supérieur droit du composant WebPart **Informations de base** , puis cliquez sur **Modifier le composant WebPart**. Ou bien, sous l’onglet **Composant WebPart** du ruban, dans le groupe **Propriétés** , cliquez sur **Propriétés de composant WebPart** pour afficher la partie editor. 
            
    4. Dans la section **Champs de projet affichés** de la partie Editor (voir la figure 1), choisissez **Modifier**.
            
    5. Ajout du champ personnalisé de **Coût de la proposition** , déplacez-le au-dessus du champ **propriétaire** dans la liste des **Champs de projet sélectionnés** , puis cliquez sur **OK** (voir Figure 1).
      
    6. Dans la partie Editor, cliquez sur **OK**, puis choisissez **Arrêter la modification** dans le groupe **Modifier**, sur l’onglet **PAGE** du ruban. La figure 2 montre le champ personnalisé **Proposal Cost** qui est ajouté à la PDP Informations sur le projet. 

    **La figure 1. Modification du composant WebPart de champs de projet dans un PDP**

    ![Modification des champs de projet de composant WebPart dans un PDP] (media/pj15_CreateWorkflowSPD_EditPDP.gif "Modification des champs de projet de composant WebPart dans un PDP")

    **Figure 2. La PDP modifiée inclut le champ personnalisé Coût de la proposition**

    ![Le PDP édité inclut le champ coût de la proposition] (media/pj15_CreateWorkflowSPD_EditedPDP.gif "Le PDP édité inclut le champ coût de la proposition")
  
4. **Étapes du flux de travail** Créez les étapes sont nécessaires pour chaque phase du flux de travail. Dans la page Paramètres du serveur, sélectionnez les **Étapes du flux de travail**, puis **Nouvelle étape de flux de travail**. La figure 3 montre une partie de la page Ajouter une étape de flux de travail.
    
    **Figure 3. Ajout d’une étape de flux de travail dans Project Web App**

    ![Ajout d’une étape de flux de travail dans Project Web App] (media/pj15_CreateWorkflowSPD_AddWorkflowStage.gif "Ajout d’une étape de flux de travail dans Project Web App")
  
    L’exemple de flux de travail de branchement utilise les quatre étapes qui sont indiquées dans le tableau 1. Dans la section **Des paramètres supplémentaires pour la Page de détails de projet Visible** de la page Ajouter une étape de flux de travail (ne pas illustrée à la Figure 3), les valeurs sont facultatives ; elles fournissent des informations sur la page État du flux de travail. Par exemple, car la PDP détails de proposition initiale requiert l’entrée utilisateur, activez la case à cocher de **la Page de détails de projet nécessitent votre attention** et puis ajouter une description spécifique telle que définie le nom du projet et de coût pour cette PDP.
    
    La figure 4 présente les quatre étapes effectuées sur la page Étapes du flux de travail.
    
    **Tableau 1. Étapes du flux de travail de branchement**

    |Nom|Description|Description de l’envoi|Phase|PDP visibles|Champs personnalisés|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |Détails de la proposition initiale  <br/> |Définir le nom du projet et le coût.  <br/> |Envoyer le projet sous la forme d’une proposition.  <br/> |Créer  <br/> |Informations sur le projet  <br/> Détails du projet  <br/> |Coût de la proposition (obligatoire)  <br/> |
    |Détails du projet  <br/> |Fournir les détails du projet proposé.  <br/> |Envoyer les détails afin de poursuivre le projet.  <br/> |Créer  <br/> |Informations sur le projet  <br/> Détails du projet  <br/> |Coût de la proposition (en lecture seule)  <br/> |
    |Refus automatique  <br/> |La proposition est rejetée d’après les informations fournies.  <br/> | <br/> |Créer  <br/> |Informations sur le projet  <br/> |Coût de la proposition (en lecture seule)  <br/> |
    |Exécution  <br/> |La proposition est acceptée et prête pour la gestion de projet.  <br/> | <br/> |Gérer  <br/> |Informations sur le projet  <br/> Détails du projet  <br/> |Coût de la proposition (en lecture seule)  <br/> |
   
    **Figure 4. Liste des étapes du flux de travail dans Project Web App**

    ![Liste des étapes du flux de travail dans Project Web App] (media/pj15_CreateWorkflowSPD_WorkflowStages.gif "Liste des étapes du flux de travail dans Project Web App")
  
#### <a name="3-construct-the-workflow-in-the-text-based-designer"></a>3. construire le flux de travail dans le Concepteur de base de texte.

Dans SharePoint Designer 2013, construisez le flux de travail à l’aide d’instructions déclaratives dans le Concepteur de base de texte. Vous pouvez commencer à taper sur la ligne d’insertion orange pour obtenir des instructions de saisie semi-automatique contextuelle pour la logique de flux de travail et les étapes, ou vous pouvez insérer la logique et les étapes à l’aide de contrôles dans le groupe **Insérer** sous l’onglet **flux de travail** du ruban. 
    
1. Dans le mode Backstage de SharePoint Designer 2013, choisissez **Ouvrir le Site**. Par exemple, ouvrez `https://ServerName/pwa`. Dans le volet de **Navigation** , choisissez **flux de travail**. Puis, sous l’onglet **flux de travail** du ruban, dans le groupe **Nouveau** , cliquez sur **Flux de travail de Site**. Cet exemple, nommez le flux de travail de création de branche de flux de travail. Vérifiez que le **Travail de SharePoint 2013 - Project Server** est activée dans la liste déroulante **Type de plateforme** (voir Figure 5). 
    
    **Figure 5. Création d’un flux de travail de site Project Server**

    ![Création d’un flux de travail Project Server] (media/pj15_CreateWorkflowSPD_CreateSiteWorkflow.gif "Création d’un flux de travail Project Server")
  
2. Sélectionnez l’onglet **Flux de travail de branchement**. Ensuite, sur l’onglet **FLUX DE TRAVAIL** du ruban, dans le groupe **Gérer**, dans la liste déroulante **Vues**, choisissez **Concepteur texte**. Pour afficher la vue avec la ligne d’insertion orange clignotante (voir la figure 6), cliquez dans la vue.
    
    **Figure 6. Utilisation de la vue du Concepteur texte pour le flux de travail**

    ![À l’aide de la vue concepteur texte] (media/pj15_CreateWorkflowSPD_TextBasedDesigner.gif "À l’aide de la vue concepteur texte")
  
3. Dans la vue du **Concepteur texte**, ajoutez les étapes utilisées par le flux de travail. Sur l’onglet **FLUX DE TRAVAIL** du ruban, dans le groupe **Insérer**, dans la liste déroulante **Étape** sous **Créer**, choisissez **Détails de la proposition initiale**.
    
    De même, placez la ligne d’insertion orange en dessous de la zone **Étape : Détails de la proposition initiale**, puis ajoutez les autres étapes utilisées par le flux de travail : **Détails du projet**, **Refus automatique** et **Exécution** (voir la figure 7). 
    
    **Figure 7. Ajout d’une étape à un flux de travail dans SharePoint Designer**

    ![Ajout d’une étape à un flux de travail dans SPD] (media/pj15_CreateWorkflowSPD_AddStageInSPD.gif "Ajout d’une étape à un flux de travail dans SPD")
  
4. Ajoutez les étapes et la logique du flux de travail pour chaque étape : 
    
    1. Pour l’étape **Détails de la proposition initiale**, placez la ligne d’insertion orange tout en haut du corps de l’étape. Dans le groupe **Insérer** du ruban, choisissez **Action**, faites défiler vers le bas jusqu’à **Actions de Project Web App**, puis choisissez **Attendre un événement de projet**. Sélectionnez **cet événement de projet**, puis **Événement : lors de la soumission d’un projet** dans la liste déroulante. 
    
    2. Dans la section **Transition vers la phase** de l’étape **Détails de la proposition initiale**, insérez **Si une valeur est égale à la valeur**. Vous pouvez commencer à saisir l’instruction ou utiliser le contrôle **Condition** dans le groupe **Insérer** du ruban. 
    
    3. Sélectionnez le premier contrôle **Valeur**, puis **fx** pour afficher la boîte de dialogue **Définir la recherche de flux de travail** (voir la figure 8). Dans la liste déroulante **Source de données**, sélectionnez **Données Projet**. Dans la liste déroulante **Champ de la source**, sélectionnez **Coût de la proposition**.
    
       **Figure 8. Définition d’une valeur de choix dans le flux de travail**

       ![Définition d’une valeur de recherche dans le flux de travail] (media/pj15_CreateWorkflowSPD_DefineWorkflowLookup.gif "Définition d’une valeur de recherche dans le flux de travail")
  
    4. Effectuer la `If` instruction afin qu’il affiche les éléments suivants : **données : proposition de projet si coût est supérieur à 25 000.**
    
       > [!NOTE]
       > Vous pouvez également créer une variable de flux de travail, définir la variable selon la valeur du champ personnalisé, puis comparer la variable à une valeur. Par exemple, à partir de la liste déroulante **Variables locales** du ruban, créez une variable nommée **TotalCost** (sans espace) de type **Number**. Dans la boîte de dialogue **Définir la recherche de flux de travail**, sélectionnez **Paramètres et variables du flux de travail** comme source de données, puis sélectionnez **Variable : TotalCost** comme champ. L’instruction **If** serait alors : **If Variable : TotalCost est supérieur à 25 000**.
  
    5. Placer la ligne d’insertion orange dans le `If` branch et insérer puis **revenez à une étape** à l’aide du contrôle de **l’Action** , dans le groupe **Insérer** sur le ruban. Sélectionnez le contrôle de liste déroulante **d’une étape** et la phase **Refus** . 
    
       De même, dans le `Else` branch, insérez l’instruction **Atteindre les détails du projet** . La figure 9 montre la fenêtre **Détails de la proposition initiale** terminée. 
    
       **Figure 9. Logique utilisée pour l’étape Détails de la proposition initiale**

       ![Logique terminé pour les détails de la proposition initiale] (media/pj15_CreateWorkflowSPD_InitialStageLogic.gif "Logique terminé pour les détails de la proposition initiale")
  
    6. Pour l’étape **Refus automatique**,  laissez la première section vide, sauf si vous voulez suspendre le flux de travail et afficher certaines données dans une PDP. La section **Transition vers la phase** doit contenir une transition ; étant donné qu’il n’existe aucune étape après un refus, saisissez Accéder à Fin du flux de travail dans l’instruction. 
    
    7. Pour l’étape **Détails du projet**, ajoutez Accéder à Exécution dans la section **Transition vers la phase**. Il n’est pas nécessaire d’attendre l’envoi d’un événement, sauf s’il existe des données supplémentaires à ajouter ou si vous voulez suspendre le flux de travail. 
    
    8. Pour l’étape **Exécution**, laissez la section de l’action de l’étape vide, sauf si vous voulez suspendre le flux de travail. Dans la section **Transition vers la phase**, ajoutez **Accéder à Fin du flux de travail**.
    
5. Dans le groupe **Enregistrer** du ruban, sélectionnez **Rechercher les erreurs** pour rechercher des erreurs de flux de travail (voir la figure 10). Corrigez les erreurs éventuelles, puis cliquez sur **Enregistrer**.
    
    **Figure 10. Rechercher des erreurs dans le flux de travail dans SharePoint Designer**

    ![Vérification des erreurs dans le flux de travail] (media/pj15_CreateWorkflowSPD_SPDCheckForErrors.gif "Vérification des erreurs dans le flux de travail")
  
6. (Facultatif) Dans le groupe **Gérer** du ruban, dans le menu déroulant **Vues**, choisissez **Concepteur visuel**. Dans la figure 11, un zoom arrière à 50 % est appliqué.
    
    Vous pouvez modifier des éléments dans le flux de travail à l’aide du Concepteur visuel. Par exemple, sélectionnez la condition **Si une valeur est égale à la valeur**, cliquez sur l’icône des outils dans le coin inférieur gauche de la condition, puis sélectionnez ** Valeur** pour afficher les conditions de comparaison dans la boîte de dialogue **Propriétés**. 
    
    **Figure 11. Utilisation du Concepteur visuel pour un flux de travail**

    ![À l’aide du mode de création de Visio du flux de travail] (media/pj15_CreateWorkflowSPD_SwitchView.gif "À l’aide du mode de création de Visio du flux de travail")
  
    Lorsque le flux de travail se trouve dans la vue du concepteur visuel, pour enregistrer le flux de travail dans un fichier Visio 2013 (.vsdx) en tant que sauvegarde ou pour une utilisation ultérieure, vous pouvez choisir **Exporter vers Visio**.
    
7. Publier le flux de travail. Lorsque vous utilisez SharePoint Designer 2013 pour publier le flux de travail sur le site Project Web App actif, le flux de travail est enregistré sur le site SharePoint ou dans Azure et devient disponible dans Project Web App pour nouveau TPE.

#### <a name="4-create-an-ept-for-the-workflow-and-then-test-the-workflow"></a>4. créer un EPT pour le flux de travail, puis tester le flux de travail.

Dans Project Web App, créez un EPT pour le flux de travail, puis tester le flux de travail en créant une proposition de projet :
    
1. Dans la page Paramètres de PWA, choisissez **Types de projets d’entreprise**, puis créez un EPT appelé flux de travail de branchement de Test. Désactivez la case à cocher **créer des projets en tant que projets de liste de tâches SharePoint** afin que Project Server conserve un contrôle total de projets qui sont créés par le TPE. Sélectionnez **Branchement le flux de travail** dans la liste déroulante **Association de flux de travail de Site** , puis sélectionnez la PDP **Informations sur le projet** dans la liste déroulante de **Page du nouveau projet** à la première page qui affiche le flux de travail. 
    
    **Figure 12. Ajout d’un type de projet d’entreprise pour le flux de travail**

    ![Ajout d’un EPT pour le flux de travail] (media/pj15_CreateWorkflowSPD_EPTs.gif "Ajout d’un EPT pour le flux de travail")
  
    > [!NOTE]
    > Lorsque la valeur **Oui** apparaît dans la colonne **Projet de liste de tâches SharePoint** du tableau des types de projet d’entreprise, cela fait référence à un EPT qui crée une liste de tâches SharePoint, où la liste de tâches est visible dans Project Web App, mais où SharePoint conserve le contrôle du projet. Pour plus d’informations sur la gestion de projets en tant que listes de tâches SharePoint, voir [Project Server 2013 architecture](project-server-2013-architecture.md). 
  
2. Ouvrez la page de projets dans Project Web App, puis créez un projet à l’aide de la nouvel TPE (voir la Figure 13). **Flux de travail de branchement de Test** étant associé au **Flux de travail branchement**, la création de projet démarre sous le contrôle du flux de travail.
    
    **Figure 13. Création d’un projet grâce à l’EPT Flux de travail de branchement de test**

    ![Création d’un projet avec TPE] (media/pj15_CreateWorkflowSPD_NewProject.gif "Création d’un projet avec TPE")
  
3. Lorsque le flux de travail affiche les **Informations sur le projet** PDP, ajoutez les données dans les champs de projet. Par exemple, entrez une valeur de **Coût de la proposition** de 30000. La version américaine de Project Server modifie le champ pour afficher les 30 000 $ (voir Figure 14).
    
    **Figure 14. Utilisation de la PDP Informations sur le projet modifiée**

    ![À l’aide de la PDP informations de projet modifiée] (media/pj15_CreateWorkflowSPD_NewProjectStage1.gif "À l’aide de la PDP informations de projet modifiée")
  
4. Sur l’onglet **PROJET** du ruban, dans le groupe **Projet**, choisissez **Enregistrer**. Project Server ajoute les données de la PDP dans le projet, puis affiche la page État du flux de travail (voir la figure 15). Pour voir la description complète de l’étape Détails de la proposition initiale dans le diagramme de l’état du flux de travail, placez le pointeur sur l’étape dans le diagramme de visualisation du flux de travail.
    
    Dans la grille **Toutes les étapes du flux de travail**, la flèche verte indique que l’étape Détails de la proposition initiale attend que l’utilisateur saisisse des informations. Cela est dû au fait que le flux de travail attend un événement d’envoi dans l’étape Détails de la proposition initiale. Si le flux de travail n’attendait pas un événement d’envoi, vous pourriez sélectionner **Suivant** dans le groupe **Page** pour passer à la PDP suivante. 
    
    **Figure 15.Utilisation de la page État du flux de travail dans l’étape Détails de la proposition initiale**

    ![Page d’état de flux de travail après la première phase] (media/pj15_CreateWorkflowSPD_NewProjectStage1Status.gif "Page d’état de flux de travail après la première phase")
  
    Le diagramme de visualisation du flux de travail affiche l’étape actuelle en vert. Dans la phase **Créer**, l’étape Détails de la proposition initiale est l’étape en cours. 
    
5. Sur le ruban, dans le groupe **Flux de travail**, cliquez sur **Envoyer**.
    
    > [!TIP]
    > Si le contrôle **Envoyer** est désactivé, actualisez la page. 
  
    Si la valeur **Coût de la proposition** est supérieure à 25 000 $ USD, le flux de travail passe à l’étape Refus automatique. La figure 16 montre l’état de l’étape Refus automatique lorsque vous cliquez à nouveau sur **Envoyer**. Si la valeur **Coût de la proposition** est inférieure ou égale à 25 000 $ USD, le flux de travail passe à l’étape Détails du projet (voir la figure 17). 
    
    **Figure 16. Le flux de travail est terminé avec l’étape Refus automatique**

    ![Le flux de travail est terminé avec refus automatique] (media/pj15_CreateWorkflowSPD_AutomatedRejectionCompleted.gif "Le flux de travail est terminé avec refus automatique")
  
    La figure 17 montre une autre test avec une proposition de projet nommée **Test 2 - branchement**, où l’étape Détails du projet est en cours de la phase de création. La phase de gestion s’affiche dans une lumière bleue couleur, ce qui indique que la phase n’est pas active.
    
    **Figure 17. Le flux de travail passe à l’étape Détails du projet si le coût est inférieur à 25 000 $**

    ![État du flux de travail à l’étape Détails du projet] (media/pj15_CreateWorkflowSPD_ProjectDetailsStage.gif "État du flux de travail à l’étape Détails du projet")
  
6. Si vous passez à l’étape Détails du projet, vous n’avez pas de données supplémentaires à ajouter dans la page par défaut. Cliquez à nouveau sur **Envoyer** pour passer à l’étape Exécution (voir la figure 18). 
    
    **Figure 18. Le flux de travail est prêt à être géré dans l’étape Exécution**

    ![État du flux de travail dans la phase d’exécution] (media/pj15_CreateWorkflowSPD_ExecutionStage.gif "État du flux de travail dans la phase d’exécution")
  
Dans l’étape Détails du projet, le flux de travail n’attend pas un événement d’envoi. Si la PDP Détails du projet comprend des champs obligatoires supplémentaires, Project Server attend que vous ajoutiez des données dans les champs avant de passer à l’étape Exécution. Comme défini dans le flux de travail de branchement, l’étape Exécution n’attend pas non plus d’événement d’envoi. Dans l’étape Exécution, vous pouvez modifier le projet en tant que responsable de projet ou choisir **Fermer** dans l’onglet **PROJET** du ruban. Lorsque vous choisissez **Fermer**, vous pouvez archiver le projet et le modifier plus tard, ou laisser le projet extrait.

Le projet **Flux de travail de branchement** est un exemple simple qui comporte un seul test de comparaison. Le flux de travail implique trois étapes dans la phase Créer et une étape dans la phase Gérer de la gestion de la demande. Pour bien tester un flux de travail, vous devez tester toutes les branches du flux de travail et utiliser des valeurs extrêmes et typiques afin de voir si le comportement est conforme à vos attentes. 

<a name="pj15_CreateWorkflowSPD_ImportingVromVisio"> </a>

## <a name="importing-a-workflow-from-visio"></a>Importation d’un flux de travail à partir de Visio

Pour modifier le flux de travail, vous pouvez créer ou modifier des champs personnalisés contrôlés par des flux de travail et créer ou modifier des étapes et phases du flux de travail. Vous pouvez utiliser SharePoint Designer 2013 pour ajouter des conditions, des actions, boucles et étapes, puis enregistrer et republier le flux de travail. Pour réutiliser ou de conserver une sauvegarde d’un flux de travail, vous pouvez l’exporter vers un fichier Visio 2013. 
  
Vous pouvez également créer ou modifier le flux de travail dans Visio 2013 et importer le fichier dans SharePoint Designer 2013 pour une utilisation par Project Web App. Pour utiliser un flux de travail non modifié, l’instance Project Web App doit inclure les propriétés de l’étape du flux de travail qui sont les mêmes que celles de l’instance Project Web App d’origine. Pour plus d’informations sur l’utilisation de Visio pour créer des flux de travail, voir [développement de flux de travail dans SharePoint Designer 2013 et Visio 2013](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx).
  
> [!NOTE]
> Lorsque vous importez un fichier Visio 2013 vers une autre instance de Project Web App, les étapes ont différents étape GUID, même si les noms d’étape sont les mêmes. Après avoir importé le flux de travail, vous devez configurer les propriétés d’étape et l’action pour utiliser les valeurs qui sont spécifiques à l’instance Project Web App. 
> 
> Si vous créez un flux de travail dans Visio 2013, les étapes et les actions n’ont aucuns propriétés qui sont spécifiques à une instance Project Web App Visio ne pas se connecter à Project Web App. Lorsque vous vous connectez à SharePoint Designer 2013 avec Project Web App, créer un flux de travail et puis pour importer le fichier VSDX, vous remplacez le flux de travail actif. Vous devez ensuite configurer les propriétés d’étape et l’action pour faire correspondre les valeurs de SharePoint Designer 2013 obtient à partir de Project Web App. 
  
### <a name="to-import-a-workflow-from-visio-to-sharepoint-designer"></a>Pour importer un flux de travail à partir de Visio dans SharePoint Designer

1. Dans Visio 2013, créez un flux de travail simple. Par exemple, procédez comme suit :
    
   1. Ouvrez Visio, puis créez un flux de travail. Choisissez le volet **CATÉGORIES** pour un nouveau flux de travail, puis sélectionnez **Diagramme de flux**, le modèle **Flux de travail Microsoft SharePoint 2013** dans le volet **Nouveau**, puis **Créer**. Le flux de travail s’ouvre avec une forme d’étape nommée **Étape 1**. Le flux de travail comprend un composant de démarrage, une forme d’entrée et une forme de sortie au sein de la forme d’étape.
    
      Lorsque vous pointez sur la forme d’étape et cliquez sur l’icône de **Propriétés** , la sélection est désactivée. Vous pouvez définir les propriétés de l’étape et l’action après avoir importé le diagramme de flux de travail SharePoint Designer 2013. 
    
      > [!NOTE]
      >  Les seuls gabarits de forme que vous devez utiliser dans la liste des formes de diagramme de flux sont les suivants : 
      > - **Actions - flux de travail SharePoint 2013**
      > - **Composants - flux de travail SharePoint 2013**
      > - **Conditions - flux de travail SharePoint 2013**
  
   2. Dans le volet **Formes**, choisissez **Formes rapides**, puis faites glisser la forme de condition nommée **Si une valeur est égale à la valeur** à droite de la forme d’étape. 
    
   3. Sur l’onglet **ACCUEIL** du ruban, choisissez l’outil **Connecteur**, puis connectez la forme de sortie de l’étape à la forme de condition (voir la figure 19). 
    
      **Figure 19. Connexion d’une forme d’étape à une forme de condition dans un diagramme de flux de travail Visio**

      ![Création d’un diagramme de flux de travail dans Visio] (media/pj15_CreateWorkflowSPD_NewVisioWorkflow.gif "Création d’un diagramme de flux de travail dans Visio")
  
   4. Faites glisser deux autres formes d’étape à droite de la forme de condition. Les formes sont nommées **Étape 2** et **Étape 3**.
    
   5. À l’aide de l’outil **connecteur** , se connecter le côté droit de la forme de Condition à la forme d’entrée de **l’étape 2**. Choisissez l’outil **pointeur** , double-cliquez sur la connexion pour afficher une zone de texte Nom, puis nommez la connexion Oui.
    
   6. Connectez le bas de la forme de condition à la forme d’entrée de **Étape 3**. À l’aide de l’outil **Pointeur**, cliquez avec le bouton droit de la souris sur la connexion, puis choisissez **Non**. Chacune de ces méthodes fonctionne pour nommer les connecteurs **Oui** ou **Non**.
    
   7. Dans le volet **formes** , choisissez **Actions - flux de travail SharePoint 2013**, puis faites glisser l’action **attendre un événement de projet** au milieu de la forme **Étape** 1 (voir la Figure 20). 
    
      **Figure 20. Réalisation du flux de travail dans Visio**

      ![À la fin du flux de travail dans Visio] (media/pj15_CreateWorkflowSPD_CompletedVisioWorkflow.gif "À la fin du flux de travail dans Visio")
  
   8. Sous l’onglet **processus** du ruban, dans le groupe de **Validation de diagramme** , sélectionnez **Vérifier le diagramme**. Corrigez les erreurs, puis enregistrez le dessin. Par exemple, nom du flux de travail de Test de fichier à partir de Visio.vsdx.
    
      Pour plus d’informations sur la résolution des erreurs de flux de travail, voir les [erreurs de validation de flux de travail de résolution des problèmes SharePoint Server 2013 dans Visio 2013](https://msdn.microsoft.com/library/jj163971%28v=office.15%29.aspx).
    
2. Ouvrez SharePoint Designer 2013, puis ouvrez le site Project Web App de même que vous avez utilisé pour l’exemple de **Flux de travail branchement** . 
    
3. Choisissez **flux de travail** dans le volet de **Navigation** , puis créer un flux de travail de site (sous l’onglet **flux de travail** du ruban, cliquez sur **Flux de travail de Site** ). Par exemple, nom du flux de travail Simple flux de travail à partir de Visio.
    
   Dans la boîte de dialogue **Créer un travail de Site** , vérifiez que le type de plateforme est de **Travail SharePoint 2013 - Project Server**. Choisissez **créer**et SharePoint Designer s’ouvre le volet **Concepteur texte** pour le nouveau workflow. 
    
4. Dans le groupe **Gérer**, sur l’onglet **FLUX DE TRAVAIL** du ruban, choisissez **Paramètres du flux de travail**.
    
5. Dans le groupe **Gérer** sous l’onglet **Paramètres de flux de travail** du ruban, cliquez sur **Importer à partir de Visio**, puis importer le fichier de **flux de travail de Test de Visio.vsdx** que vous avez précédemment enregistré. Une boîte de dialogue **Microsoft SharePoint Designer** vous avertit que le diagramme que vous importez contient pas de propriétés du flux de travail et vous demande si vous souhaitez écraser le flux de travail en cours. Cliquez sur **Oui**. Importe le diagramme de flux de travail, SharePoint Designer génère des formes de gabarits et affiche le volet de **Concepteur visuel** qui contient le flux de travail importé. 
    
6. Définir les propriétés de chaque forme d’étape dans le flux de travail. Par exemple, la première forme de la fenêtre de partage est appelée **étape 1 (non valide)**, car elle ne représente pas une étape valide dans l’instance de Project Web App connectée. Lorsque vous sélectionnez ou pointez sur la fenêtre de partage, vous pouvez choisir l’icône de **Propriétés** en bas à gauche de la forme d’étape pour afficher la boîte de dialogue **Propriétés de l’étape** zone (voir la Figure 21). Sélectionnez la phase **Détails de la proposition initiale** dans la liste déroulante **Étape du projet** , puis cliquez sur **OK**. SharePoint Designer renomme la fenêtre de partage.
    
   **Figure 21. Définition des propriétés de l’étape dans SharePoint Designer**

   ![Définition des propriétés dans un flux de travail importé] (media/pj15_CreateWorkflowSPD_ImportFromVisio1.gif "Définition des propriétés dans un flux de travail importé")
  
   Pour la deuxième étape, définissez la propriété **Phase de projet** sur **Refus automatique**. Pour la troisième étape, définissez la propriété **Phase de projet** sur **Exécution**.
    
7. De même, pour l’action **Attendre un événement de projet**, définissez la propriété **Nom de l’événement** sur **Événement : lors de la soumission d’un projet**.
    
8. De même, définissez les propriétés de la condition **Si n’importe quelle valeur est égale à la valeur** . Par exemple, définissez la première propriété de **valeur** au **Coût de données : proposition de projet**. Affectez à la propriété **opérateur** **est inférieure à**. Définissez la propriété **Value** deuxième à 5000.
    
9. Vérifiez que le flux de travail ne comporte pas d’erreur, puis enregistrez-le. Si aucune erreur n’est détectée, vous pouvez passer à la vue du **Concepteur texte** (voir la figure 22). 
    
   **Figure 22. Affichage du flux de travail importé dans le Concepteur texte**

   ![Affichage du flux de travail importé] (media/pj15_CreateWorkflowSPD_WorkflowFromVisio.gif "Affichage du flux de travail importé")
  
10. Publiez le flux de travail. Si vous enregistrez le flux de travail, mais que vous ne le publiez pas, il ne sera pas disponible lorsque vous créerez un type de projet d’entreprise.
    
11. Pour tester le **flux de travail Simple à partir de Visio** importé dans Project Web App, créez un TPE qui utilise le flux de travail et puis créer des projets qui utilisent le nouveau TPE comme dans l’exemple de **Flux de travail branchement** . Dans ce cas, toutefois, les projets qui sont inférieures à 5 000 $ coût sont rejetées. 
    
Dans l’utilisation par le biais de cet article, vous créé et testé un flux de travail de branchement simple à l’aide de SharePoint Designer 2013 pour définir directement les étapes, les conditions et les actions qui utilise le flux de travail. Vous avez également créé un diagramme d’un flux de travail de branchement encore plus simple à l’aide de Visio 2013. Vous avez importé le diagramme de flux de travail Visio dans SharePoint Designer 2013, où vous définissez les propriétés de chaque étape, une condition et une action à partir de la connexion à Project Web App.
  
Visio 2013 et SharePoint Designer ensemble permettent de pratique pour les concepteurs, les responsables de projets, les développeurs de flux de travail et les testeurs à créer, partager et personnaliser des modèles de flux de travail pour les installations différentes de Project Server 2013 et Project Online. Pour les flux de travail qui nécessite un accès par programme à Project Server qui ne fournit pas de SharePoint Designer, vous pouvez utiliser Visual Studio 2012 avec le modèle objet côté client (CSOM).
  
## <a name="see-also"></a>Voir aussi

- [Architecture Project Server 2013](project-server-2013-architecture.md)
- [Démarrage : Installer et configurer le Gestionnaire de workflow SharePoint 2013](https://msdn.microsoft.com/library/jj163276%28office.15%29.aspx)
- [Comprendre comment empaqueter et déployer des flux de travail dans SharePoint 2013](https://msdn.microsoft.com/library/jj819316%28office.15%29.aspx)
- [Flux de travail dans SharePoint 2013](https://msdn.microsoft.com/library/jj163986%28office.15%29.aspx)
- [Développement de flux de travail dans SharePoint Designer 2013 et Visio 2013](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
- [Dépannage des erreurs de validation de flux de travail SharePoint Server 2013 dans Visio 2013](https://msdn.microsoft.com/library/jj163971%28v=office.15%29.aspx)
- [Flux de travail et de gestion de la demande](https://msdn.microsoft.com/library/cf7433a3-a531-4467-ac0c-df0c5d6881ae%28Office.15%29.aspx)

