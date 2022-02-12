---
title: Création d’un flux de travail Project Server pour la gestion de la demande
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: b0e4a3b3-d1df-454d-b74c-b980b0b456f6
description: Cet article explique comment créer un flux de travail simple à l’aide de SharePoint Designer 2013.
ms.openlocfilehash: b51036d1b2ba332841d6779773b0e31afd3998b7
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62781190"
---
# <a name="create-a-project-server-workflow-for-demand-management"></a>Création d’un flux de travail Project Server pour la gestion de la demande

Cet article explique comment créer un flux de travail simple à l’aide de SharePoint Designer 2013. Vous pouvez exporter le flux de travail vers Visio 2013 pour la visualisation et la modification, ou utiliser Visio 2013 pour concevoir des flux de travail Project Server 2013 et importer la conception dans SharePoint Designer 2013 pour la publication dans Project Web App. Pour plus d’informations sur la plateforme de flux de travail SharePoint et la création de flux de travail avec Visio 2013 et SharePoint Designer 2013, voir les articles flux de travail dans [SharePoint 2013](https://msdn.microsoft.com/library/jj163986%28office.15%29.aspx) dans la documentation du développeur SharePoint 2013. 
  
Pour plus d’informations sur la préparation Project Server pour les flux de travail, voir Start[: Set up and configure SharePoint 2013 Gestionnaire de flux de travail](https://msdn.microsoft.com/library/jj163276%28office.15%29.aspx).

<a name="pj15_CreateWorkflowSPD_General"> </a>

## <a name="creating-a-general-workflow"></a>Création d’un flux de travail général

Utilisez les étapes suivantes pour créer un flux Project Server 2013 à l’aide de SharePoint Designer 2013. Le flux de travail est conçu pour la gestion de la demande des propositions de projet.
  
Pour obtenir la procédure détaillée, consultez la section [Création d’un flux de travail de branchement](#pj15_CreateWorkflowSPD_Detailed) . 
  
### <a name="to-create-a-project-server-workflow-general-procedure"></a>Pour créer un flux de travail Project Server (procédure générale)

1. Déterminez les conditions requises et concevez le flux de travail. Organisez-le par phases et par étapes, puis déterminez les champs personnalisés qu’il utilisera.
    
2. Dans Project Web App, créez les entités dont le flux de travail a besoin :
    
    1. Passez en revue les phases de flux de travail existantes et créez-en d’autres si nécessaire.
        
    2. Créez les champs personnalisés d’entreprise que le flux de travail utilisera. Pour être disponible dans l’étape d’un flux de travail, un champ personnalisé doit être contrôlé par un flux de travail.
        
    3. Modifiez ou créez les pages de détails de projet (PDP) que les étapes de votre flux de travail utiliseront en vue de recueillir des informations pour le projet. Dans cet exemple, les étapes utilisent des PDP par défaut, modifiées pour inclure un nouveau champ personnalisé.
        
    4. Créez les étapes du flux de travail nécessaires, puis associez chacun d’elle à la phase appropriée.
    
3. Dans SharePoint Designer 2013, construisez le flux de travail à l’aide d’instructions déclaratives dans le concepteur **textuel** :
    
    > [!NOTE]
    > Vous pouvez également basculer vers le  concepteur visuel dans SharePoint Designer 2013 ou importer un flux de travail existant à partir Visio 2013. Procédez comme suit pour utiliser le **Concepteur texte** : 
    > 
    > 1. Ouvrez le site Project Web App, puis créez un flux de travail de site qui utilise la plateforme de flux de travail **SharePoint 2013 Project Server**. 
    > 2. Ajoutez les étapes utilisées par le flux de travail.
    > 3. Insérez les étapes, les conditions, les actions et les boucles du flux de travail requises à chaque étape.
    > 4. Recherchez les éventuelles erreurs de flux de travail et corrigez-les si vous en détectez.
    > 5. (Facultatif) Basculez l’affichage vers **le Concepteur** visuel ou exportez le flux de travail vers un Visio 2013. Vous pouvez modifier l’affichage Visio et enregistrer les modifications dans le flux de travail actuel. Vous pouvez modifier le fichier Visio et l’importer dans SharePoint Designer 2013 pour créer d’autres flux de travail.
    > 6. Publiez le flux de travail. Une fois publié, le flux de travail s’affiche dans la liste des flux de travail pour Project Web App site.
    
4. Dans Project Web App, utilisez le flux de travail pour la gestion de la demande des propositions de projet :
    
    1. Créez un modèle de projet d’entreprise (EPT) qui utilise le flux de travail.
        
    2. Sur la page du centre de projets, créez un projet qui utilise l’EPT pour le flux de travail, puis suivez les étapes du flux de travail.
        
    3. Testez rigoureusement le flux de travail.
        
    4. Déployez le flux de travail sur un serveur de production.

<a name="pj15_CreateWorkflowSPD_Detailed"> </a>

## <a name="creating-a-branching-workflow"></a>Création d’un flux de travail de branchement

Avant de pouvoir utiliser SharePoint Designer 2013 pour créer un flux de travail Project Server, le service Gestionnaire de flux de travail Client 1.0 doit être configuré pour utiliser les activités de flux de travail Project Server 2013. Pour plus d’informations sur la configuration de Gestionnaire de flux de travail Client 1.0, voir les articles Flux de travail dans [SharePoint 2013](https://msdn.microsoft.com/library/jj163986%28office.15%29.aspx) de la documentation du développeur SharePoint Server 2013. 
  
La procédure détaillée suivante comprend les mêmes étapes que dans la section [Création d’un flux de travail](#pj15_CreateWorkflowSPD_General) général. 
  
### <a name="to-create-a-project-server-branching-workflow-detailed-procedure"></a>Pour créer un flux de travail de branchement Project Server (procédure détaillée)

#### <a name="1-plan-and-design-the-workflow"></a>1. Planifiez et concevez le flux de travail.

Un flux de travail Project Server peut s’intégrer à plusieurs étapes et phases d’un processus de gestion de la demande. Du fait de la complexité des flux de travail, vous devez comprendre les impératifs de l’entreprise et planifier un flux de travail attentivement. Pour prendre un exemple simple, concevez un flux de travail de branchement qui utilise le coût estimé d’une proposition de projet afin de déterminer si la proposition est acceptée. Si le coût estimé est supérieur à 25 000 $ USD, rejetez la proposition ; dans le cas contraire, acceptez la proposition et créez le projet.
    
Étant donné que vous pouvez utiliser Visio 2013 et SharePoint Designer 2013 pour vous aider à concevoir et créer des flux de travail pour Project Server 2013, vous pouvez tester plus facilement les flux de travail qu’avec Project Server 2010. L’exemple de conception de flux de travail dans cet article est le même que dans [l’article Créer](https://msdn.microsoft.com/library/a02cafdc-d881-4271-b446-d8b2cd456a52%28Office.15%29.aspx) un flux de travail de branchement dans le SDK Project 2010. Vous pouvez concevoir et créer un flux de travail de test sur un ordinateur distant à l’aide d’une instance de test de Project Web App ; vous n’avez pas besoin de créer de flux de travail directement sur un ordinateur Project Server 2013. 
    
#### <a name="2-create-the-entities-that-your-workflow-requires"></a>2. Créez les entités dont votre flux de travail a besoin.

Dans Project Web App, examinez les phases et étapes de flux de travail disponibles, ainsi que les champs personnalisés d’entreprise disponibles. Si nécessaire, créez les entités requises par votre flux de travail, comme indiqué dans les étapes suivantes :
    
1. **Phases de flux de travail** L’installation par Project Web App inclut les phases Créer, Sélectionner, Planifier, Gérer et Terminé. Pour l’exemple du flux de travail de branchement, il est inutile de créer d’autres phases. 
        
2. **Enterprise champs personnalisés** Le flux de travail de branchement nécessite un champ personnalisé de coût de projet contrôlé par le flux de travail. La valeur d’un champ personnalisé contrôlé par un flux de travail est définie dans une PDP utilisée par le flux de travail. Par exemple, choisissez **l’icône Paramètres** en haut à droite d’une page Project Web App, choisissez **PWA Paramètres**, puis Enterprise Champs personnalisés et Tables de **choix**.
        
   Créez un champ personnalisé nommé Coût de la proposition pour l’entité **Projet**, puis sélectionnez le type **Coût**. Pour la description, entrez Coût estimé d’une proposition de projet. Dans la section **Comportement**, choisissez **Comportement contrôlé par flux de travail**.
        
3. **Project pages de détails** Modifiez ou créez les PDP que les étapes du flux de travail utiliseront. Par exemple, procédez comme suit : 
        
    1. Sélectionnez **Pages de détails de projet** sur la page Paramètres du serveur, puis choisissez la PDP **Informations sur le projet**. 
            
    2. Sur l’onglet **PAGE** du ruban, dans le groupe **Modifier**, choisissez **Modifier la page**.
            
    3. Sélectionnez la flèche vers le bas en haut à droite du **volet Web Informations** de base, puis sélectionnez **Modifier le volet Web**. Ou, sous **l’onglet WEB PART** du ruban, dans le groupe **Propriétés** , choisissez Propriétés du site **Web** Part pour afficher le partie d’éditeur. 
            
    4. Dans la section **Champs de projet affichés** de la partie Editor (voir la figure 1), choisissez **Modifier**.
            
    5. Ajoutez **le champ personnalisé Coût** de proposition, déplacez-le au-dessus  du champ Propriétaire dans la liste Champs Project sélectionnés, puis choisissez **OK** (voir figure 1).
      
    6. Dans la partie Editor, cliquez sur **OK**, puis choisissez **Arrêter la modification** dans le groupe **Modifier**, sur l’onglet **PAGE** du ruban. La figure 2 montre le champ personnalisé **Proposal Cost** qui est ajouté à la PDP Informations sur le projet. 

    **Figure 1. Modification du Project web Fields dans une PDP**

    ![Modification du Project web Fields dans une PDP](media/pj15_CreateWorkflowSPD_EditPDP.gif "Modification du Project web Fields dans une PDP")

    **Figure 2. La PDP modifiée inclut le champ personnalisé Coût de la proposition**

    ![La PDP modifiée inclut le champ de coût de la proposition](media/pj15_CreateWorkflowSPD_EditedPDP.gif "La PDP modifiée inclut le champ de coût de la proposition")
  
4. **Étapes du flux de travail** Créez les étapes requises pour chaque phase du flux de travail. Sur la page Paramètres du serveur, sélectionnez **Étapes du flux de travail**, puis **NOUVELLE ÉTAPE DE FLUX DE TRAVAIL**. La figure 3 montre une partie de la page Ajouter une étape de flux de travail.
    
    **Figure 3. Ajout d’une étape de flux de travail dans Project Web App**

    ![Ajout d’une étape de flux de travail dans Project Web App](media/pj15_CreateWorkflowSPD_AddWorkflowStage.gif "Ajout d’une étape de flux de travail dans Project Web App")
  
    L’exemple du flux de travail de branchement utilise les quatre étapes présentées dans le tableau 1. Dans la section **Paramètres supplémentaires pour la page de détails de projet visible** de la page Ajouter une étape de flux de travail (non illustrée dans la figure 3), les valeurs sont facultatives ; elles fournissent plus d’informations sur la page État du flux de travail. Par exemple, étant donné que la PDP Détails de la proposition initiale nécessite une entrée de l’utilisateur, vous pouvez cocher La page de détails Project nécessite une **attention** particulière, puis ajouter une description spécifique telle que Définir le nom et le coût du projet pour cette PDP.
    
    La figure 4 présente les quatre étapes effectuées sur la page Étapes du flux de travail.
    
    **Tableau 1. Étapes du flux de travail de branchement**

    |Nom|Description|Description de l’envoi|Phase|PDP visibles|Champs personnalisés|
    |:-----|:-----|:-----|:-----|:-----|:-----|
    |Détails de la proposition initiale  <br/> |Définir le nom du projet et le coût. |Envoyer le projet sous la forme d’une proposition. |Créer  <br/> |Informations sur le projet  <br/> Détails du projet  <br/> |Coût de la proposition (obligatoire)  <br/> |
    |Détails du projet  <br/> |Fournir les détails du projet proposé. |Envoyer les détails afin de poursuivre le projet. |Créer  <br/> |Informations sur le projet  <br/> Détails du projet  <br/> |Coût de la proposition (en lecture seule)  <br/> |
    |Refus automatique  <br/> |La proposition est rejetée d’après les informations fournies. | <br/> |Créer  <br/> |Informations sur le projet  <br/> |Coût de la proposition (en lecture seule)  <br/> |
    |Exécution  <br/> |La proposition est acceptée et prête pour la gestion de projet. | <br/> |Gestion  <br/> |Informations sur le projet  <br/> Détails du projet  <br/> |Coût de la proposition (en lecture seule)  <br/> |
   
    **Figure 4. Liste des étapes du flux de travail dans Project Web App**

    ![Liste des étapes du flux de travail dans Project Web App](media/pj15_CreateWorkflowSPD_WorkflowStages.gif "Liste des étapes du flux de travail dans Project Web App")
  
#### <a name="3-construct-the-workflow-in-the-text-based-designer"></a>3. Construisez le flux de travail dans Text-Based Designer.

Dans SharePoint Designer 2013, construisez le flux de travail à l’aide d’instructions déclaratives dans Text-Based Designer. Vous pouvez commencer à taper sur la ligne d’insertion orange pour obtenir des instructions d’achèvement automatique contextibles pour la logique et les étapes du flux de travail, ou vous pouvez insérer  la logique et les étapes à l’aide de contrôles dans le groupe Insérer sous l’onglet **FLUX** de travail du ruban. 
    
1. Dans le mode Backstage de SharePoint Designer 2013, choisissez **Ouvrir le site**. Par exemple, ouvrez  `https://ServerName/pwa`. Dans le volet **Navigation**, choisissez **Flux de travail**. Ensuite, sur l’onglet **FLUX DE TRAVAIL** du ruban, dans le groupe **Nouveau**, sélectionnez **Flux de travail de site**. Pour cet exemple, nommez le flux de travail Flux de travail de branchement. **Assurez-vous SharePoint Flux de travail 2013 - Project Server** est sélectionné dans la liste de listes de  listes listes de types de plateforme (voir la figure 5). 
    
    **Figure 5. Création d’un flux de travail de site Project Server**

    ![Création d’un flux de travail de site Project Server](media/pj15_CreateWorkflowSPD_CreateSiteWorkflow.gif "Création d’un flux de travail de site Project Server")
  
2. Sélectionnez l’onglet **Flux de travail de branchement**. Ensuite, sur l’onglet **FLUX DE TRAVAIL** du ruban, dans le groupe **Gérer**, dans la liste déroulante **Vues**, choisissez **Concepteur texte**. Pour afficher la vue avec la ligne d’insertion orange clignotante (voir la figure 6), cliquez dans la vue.
    
    **Figure 6. Utilisation de la vue du Concepteur texte pour le flux de travail**

    ![Utilisation du Concepteur textuel](media/pj15_CreateWorkflowSPD_TextBasedDesigner.gif "Utilisation du Concepteur textuel")
  
3. Dans la vue du **Concepteur texte**, ajoutez les étapes utilisées par le flux de travail. Sur l’onglet **FLUX DE TRAVAIL** du ruban, dans le groupe **Insérer**, dans la liste déroulante **Étape** sous **Créer**, choisissez **Détails de la proposition initiale**.
    
    De même, placez la ligne d’insertion orange en dessous de la zone **Étape : Détails de la proposition initiale**, puis ajoutez les autres étapes utilisées par le flux de travail : **Détails du projet**, **Refus automatique** et **Exécution** (voir la figure 7). 
    
    **Figure 7. Ajout d’une étape à un flux de travail dans SharePoint Designer**

    ![Ajout d’une étape à un flux de travail dans SPD](media/pj15_CreateWorkflowSPD_AddStageInSPD.gif "Ajout d’une étape à un flux de travail dans SPD")
  
4. Ajoutez les étapes et la logique du flux de travail pour chaque étape : 
    
    1. Pour l’étape **Détails de la proposition initiale**, placez la ligne d’insertion orange tout en haut du corps de l’étape. Dans le groupe **Insérer** du ruban, choisissez **Action**, faites défiler vers le bas jusqu’à **Actions de Project Web App**, puis choisissez **Attendre un événement de projet**. Sélectionnez **cet événement de projet**, puis **Événement : lors de la soumission d’un projet** dans la liste déroulante. 
    
    2. Dans la section **Transition vers la phase** de l’étape **Détails de la proposition initiale**, insérez **Si une valeur est égale à la valeur**. Vous pouvez commencer à saisir l’instruction ou utiliser le contrôle **Condition** dans le groupe **Insérer** du ruban. 
    
    3. Sélectionnez le premier contrôle **Valeur**, puis **fx** pour afficher la boîte de dialogue **Définir la recherche de flux de travail** (voir la figure 8). Dans la liste déroulante **Source de données**, sélectionnez **Données Projet**. Dans la liste déroulante **Champ de la source**, sélectionnez **Coût de la proposition**.
    
       **Figure 8. Définition d’une valeur de choix dans le flux de travail**

       ![Définition d’une valeur de choix dans le flux de travail](media/pj15_CreateWorkflowSPD_DefineWorkflowLookup.gif "Définition d’une valeur de choix dans le flux de travail")
  
    4. Complétez `If` l’instruction de sorte qu’elle affiche les informations suivantes : **si Project Data:Proposal Cost est supérieur à 25 000**
    
       > [!NOTE]
       > Vous pouvez également créer une variable de flux de travail, définir la variable selon la valeur du champ personnalisé, puis comparer la variable à une valeur. Par exemple, à partir de la liste déroulante **Variables locales** du ruban, créez une variable nommée **TotalCost** (sans espace) de type **Number**. Dans la boîte de dialogue **Définir la recherche de flux de travail**, sélectionnez **Paramètres et variables du flux de travail** comme source de données, puis sélectionnez **Variable : TotalCost** comme champ. L’instruction **If** serait alors : **If Variable : TotalCost est supérieur à 25 000**.
  
    5. Placez la ligne d’insertion orange `If` dans la branche, puis  insérez Aller à une étape à l’aide  du contrôle **Action**, dans le groupe Insérer sur le ruban. Choisissez le contrôle déroulant **une étape** et sélectionnez l’étape **Refus automatique**. 
    
       De même, dans la branche`Else`, insérez **l’instruction Project détails**. La figure 9 montre l’étape **Détails de la proposition initiale** une fois terminée. 
    
       **Figure 9. Logique utilisée pour l’étape Détails de la proposition initiale**

       ![Logique utilisée pour les détails de proposition initiale](media/pj15_CreateWorkflowSPD_InitialStageLogic.gif "Logique utilisée pour les détails de proposition initiale")
  
    6. Pour l’étape **Refus automatique**,  laissez la première section vide, sauf si vous voulez suspendre le flux de travail et afficher certaines données dans une PDP. La section **Transition vers la phase** doit contenir une transition ; étant donné qu’il n’existe aucune étape après un refus, saisissez Accéder à Fin du flux de travail dans l’instruction. 
    
    7. Pour l’étape **Détails du projet**, ajoutez Accéder à Exécution dans la section **Transition vers la phase**. Il n’est pas nécessaire d’attendre l’envoi d’un événement, sauf s’il existe des données supplémentaires à ajouter ou si vous voulez suspendre le flux de travail. 
    
    8. Pour l’étape **Exécution**, laissez la section de l’action de l’étape vide, sauf si vous voulez suspendre le flux de travail. Dans la section **Transition vers la phase**, ajoutez **Accéder à Fin du flux de travail**.
    
5. Dans le groupe **Enregistrer** du ruban, sélectionnez **Rechercher les erreurs** pour rechercher des erreurs de flux de travail (voir la figure 10). Corrigez les erreurs éventuelles, puis cliquez sur **Enregistrer**.
    
    **Figure 10. Rechercher des erreurs dans le flux de travail dans SharePoint Designer**

    ![Contrôle des erreurs dans le flux de travail](media/pj15_CreateWorkflowSPD_SPDCheckForErrors.gif "Contrôle des erreurs dans le flux de travail")
  
6. (Facultatif) Dans le groupe **Gérer** du ruban, dans le menu déroulant **Vues**, choisissez **Concepteur visuel**. Dans la figure 11, un zoom arrière à 50 % est appliqué.
    
    Vous pouvez modifier des éléments dans le flux de travail à l’aide du Concepteur visuel. Par exemple, sélectionnez la condition **Si une valeur est égale à la valeur**, cliquez sur l’icône des outils dans le coin inférieur gauche de la condition, puis sélectionnez **Valeur** pour afficher les conditions de comparaison dans la boîte de dialogue **Propriétés**. 
    
    **Figure 11. Utilisation du Concepteur visuel pour un flux de travail**

    ![Utilisation du mode Création Visio pour le flux de travail](media/pj15_CreateWorkflowSPD_SwitchView.gif "Utilisation du mode Création Visio pour le flux de travail")
  
    Lorsque le flux de travail est dans l’affichage concepteur visuel, pour enregistrer le flux de travail dans un fichier Visio 2013 (.vsdx) en tant que sauvegarde ou pour une utilisation ultérieure, vous pouvez choisir d’exporter **vers Visio**.
    
7. Publiez le flux de travail. Lorsque vous utilisez SharePoint Designer 2013 pour publier le flux de travail sur le site Project Web App actif, le flux de travail est inscrit sur le site SharePoint ou dans Azure et devient disponible dans Project Web App pour les nouveaux EPT.

#### <a name="4-create-an-ept-for-the-workflow-and-then-test-the-workflow"></a>4. Créez un EPT pour le flux de travail, puis testez le flux de travail.

Dans Project Web App, créez un EPT pour le flux de travail, puis testez le flux de travail en créant une proposition de projet :
    
1. Dans la page PWA Paramètres, choisissez Enterprise Project **types**, puis créez un ept nommé Flux de travail de branchement de test. Désélectionnez la case **Créer des projets en tant que projets de liste de tâches SharePoint** afin que Project Server conserve le contrôle total des projets créés par l’EPT. Sélectionnez **Flux de travail de branchement** dans la liste déroulante **Association de flux de travail de site**, puis sélectionnez la PDP **Informations sur le projet** dans la liste déroulante **Nouvelle page de projet** afin que ce soit la première page à s’afficher dans le flux de travail. 
    
    **Figure 12. Ajout d’un type de projet d’entreprise pour le flux de travail**

    ![Ajout d’un type de projet d’entreprise pour le flux de travail](media/pj15_CreateWorkflowSPD_EPTs.gif "Ajout d’un type de projet d’entreprise pour le flux de travail")
  
    > [!NOTE]
    > Lorsque la valeur **Oui** apparaît dans la colonne **Projet de liste de tâches SharePoint** du tableau des types de projet d’entreprise, cela fait référence à un EPT qui crée une liste de tâches SharePoint, où la liste de tâches est visible dans Project Web App, mais où SharePoint conserve le contrôle du projet. Pour plus d’informations sur la gestion de projets en tant que listes de tâches SharePoint, voir [Project Server 2013 architecture](project-server-2013-architecture.md). 
  
2. Ouvrez la page Projets dans Project Web App, puis créez un projet à l’aide du nouvel EPT (voir figure 13). Étant donné que **Flux de travail de branchement de test** est associé à **Flux de travail de branchement**, la création du projet commence sous le contrôle du flux de travail.
    
    **Figure 13. Création d’un projet grâce à l’EPT Flux de travail de branchement de test**

    ![Création d’un projet avec le type de projet d’entreprise](media/pj15_CreateWorkflowSPD_NewProject.gif "Création d’un projet avec le type de projet d’entreprise")
  
3. Lorsque le flux de travail affiche la PDP **Informations sur le projet**, ajoutez des données aux champs du projet. Par exemple, entrez une **valeur de** coût de proposition de 30 000. La version américaine de Project Server modifie le champ pour afficher 30 000 $ (voir la figure 14).
    
    **Figure 14. Utilisation de la PDP Informations sur le projet modifiée**

    ![Utilisation de la PDP des informations de projet modifiée](media/pj15_CreateWorkflowSPD_NewProjectStage1.gif "Utilisation de la PDP des informations de projet modifiée")
  
4. Sur l’onglet **PROJET** du ruban, dans le groupe **Projet**, choisissez **Enregistrer**. Project Server ajoute les données de la PDP dans le projet, puis affiche la page État du flux de travail (voir la figure 15). Pour voir la description complète de l’étape Détails de la proposition initiale dans le diagramme de l’état du flux de travail, placez le pointeur sur l’étape dans le diagramme de visualisation du flux de travail.
    
    Dans la grille **Toutes les étapes du flux de travail**, la flèche verte indique que l’étape Détails de la proposition initiale attend que l’utilisateur saisisse des informations. Cela est dû au fait que le flux de travail attend un événement d’envoi dans l’étape Détails de la proposition initiale. Si le flux de travail n’attendait pas un événement d’envoi, vous pourriez sélectionner **Suivant** dans le groupe **Page** pour passer à la PDP suivante. 
    
    **Figure 15.Utilisation de la page État du flux de travail dans l’étape Détails de la proposition initiale**

    ![Page d’état du flux de travail après la première phase](media/pj15_CreateWorkflowSPD_NewProjectStage1Status.gif "Page d’état du flux de travail après la première phase")
  
    Le diagramme de visualisation du flux de travail affiche l’étape actuelle en vert. Dans la phase **Créer**, l’étape Détails de la proposition initiale est l’étape en cours. 
    
5. Sur le ruban, dans le groupe **Flux de travail**, cliquez sur **Envoyer**.
    
    > [!TIP]
    > Si le contrôle **Envoyer** est désactivé, actualisez la page. 
  
    Si la valeur **Coût de la proposition** est supérieure à 25 000 $ USD, le flux de travail passe à l’étape Refus automatique. La figure 16 montre l’état de l’étape Refus automatique lorsque vous cliquez à nouveau sur **Envoyer**. Si la valeur **Coût de la proposition** est inférieure ou égale à 25 000 $ USD, le flux de travail passe à l’étape Détails du projet (voir la figure 17). 
    
    **Figure 16. Le flux de travail est terminé avec l’étape Refus automatique**

    ![Le flux de travail est terminé avec Refus automatique](media/pj15_CreateWorkflowSPD_AutomatedRejectionCompleted.gif "Le flux de travail est terminé avec Refus automatique")
  
    La figure 17 montre un autre test avec une proposition de projet nommée **Test 2 - Branchement**, où l’étape Project détails est en cours dans la phase De création. La phase Gérer apparaît en bleu clair, ce qui indique que la phase n’est pas encore active.
    
    **Figure 17. Le flux de travail passe à l’étape Détails du projet si le coût est inférieur à 25 000 $**

    ![État du flux de travail à l’étape des détails de projet](media/pj15_CreateWorkflowSPD_ProjectDetailsStage.gif "État du flux de travail à l’étape des détails de projet")
  
6. Si vous passez à l’étape Détails du projet, vous n’avez pas de données supplémentaires à ajouter dans la page par défaut. Cliquez à nouveau sur **Envoyer** pour passer à l’étape Exécution (voir la figure 18). 
    
    **Figure 18. Le flux de travail est prêt à être géré dans l’étape Exécution**

    ![État du flux de travail dans la phase d’exécution](media/pj15_CreateWorkflowSPD_ExecutionStage.gif "État du flux de travail dans la phase d’exécution")
  
Dans l’étape Détails du projet, le flux de travail n’attend pas un événement d’envoi. Si la PDP Détails du projet comprend des champs obligatoires supplémentaires, Project Server attend que vous ajoutiez des données dans les champs avant de passer à l’étape Exécution. Comme défini dans le flux de travail de branchement, l’étape Exécution n’attend pas non plus d’événement d’envoi. Dans l’étape Exécution, vous pouvez modifier le projet en tant que responsable de projet ou choisir **Fermer** dans l’onglet **PROJET** du ruban. Lorsque vous choisissez **Fermer**, vous pouvez archiver le projet et le modifier plus tard, ou laisser le projet extrait.

Le projet **Flux de travail de branchement** est un exemple simple qui comporte un seul test de comparaison. Le flux de travail implique trois étapes dans la phase Créer et une étape dans la phase Gérer de la gestion de la demande. Pour bien tester un flux de travail, vous devez tester toutes les branches du flux de travail et utiliser des valeurs extrêmes et typiques afin de voir si le comportement est conforme à vos attentes. 

<a name="pj15_CreateWorkflowSPD_ImportingVromVisio"> </a>

## <a name="importing-a-workflow-from-visio"></a>Importation d’un flux de travail à partir de Visio

Pour modifier le flux de travail, vous pouvez créer ou modifier des champs personnalisés contrôlés par un flux de travail et créer ou modifier des phases et des étapes du flux de travail. Vous pouvez utiliser SharePoint Designer 2013 pour ajouter des conditions, des actions, des boucles et des étapes, puis enregistrer et republier le flux de travail. Pour réutiliser ou conserver une sauvegarde d’un flux de travail, vous pouvez l’exporter vers un Visio 2013. 
  
Vous pouvez également créer ou modifier le flux de travail dans Visio 2013 et importer le fichier dans SharePoint Designer 2013 pour l’utiliser Project Web App. Pour utiliser un flux de travail nonmodifié, l’instance Project Web App doit inclure des propriétés de phase de flux de travail identiques à celles de l’instance Project Web App d’origine. Pour plus d’informations sur l’utilisation de Visio pour créer des flux de travail, voir Développement de flux de travail dans [SharePoint Designer 2013 et Visio 2013](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx).
  
> [!NOTE]
> Lorsque vous importez un fichier Visio 2013 dans une instance différente de Project Web App, les étapes ont différents GUID d’étape, même si les noms des étapes sont identiques. Après avoir importé le flux de travail, vous devez configurer les propriétés de l’étape et de l’action pour utiliser des valeurs spécifiques à l Project Web App instance. 
> 
> Si vous créez un flux de travail dans Visio 2013, les étapes et les actions n’ont aucune propriété spécifique à une instance de Project Web App, car Visio ne se connecte pas à Project Web App. Lorsque vous connectez SharePoint Designer 2013 à Project Web App, créez un flux de travail, puis importez le fichier VSDX, vous devez le faire. Vous devez ensuite configurer les propriétés d’étape et d’action de manière à ce qu’SharePoint Designer 2013 obtient des Project Web App. 
  
### <a name="to-import-a-workflow-from-visio-to-sharepoint-designer"></a>Pour importer un flux de travail à partir de Visio dans SharePoint Designer

1. Dans Visio 2013, créez un flux de travail simple. Par exemple, procédez comme suit :
    
   1. Ouvrez Visio, puis créez un flux de travail. Choisissez le volet **CATÉGORIES** pour un nouveau flux de travail, puis sélectionnez **Diagramme de flux**, le modèle **Flux de travail Microsoft SharePoint 2013** dans le volet **Nouveau**, puis **Créer**. Le flux de travail s’ouvre avec une forme d’étape nommée **Étape 1**. Le flux de travail comprend un composant de démarrage, une forme d’entrée et une forme de sortie au sein de la forme d’étape.
    
      Lorsque vous passez le curseur sur la forme d’étape et que vous cliquez sur l’icône **Propriétés**, la sélection est désactivée. Vous pouvez définir les propriétés de phase et d’action après avoir importé le diagramme de flux de travail dans SharePoint Designer 2013. 
    
      > [!NOTE]
      >  Les seuls gabarits de forme que vous devez utiliser dans la liste des formes de diagramme de flux sont les suivants : 
      > - **Actions : SharePoint flux de travail 2013**
      > - **Composants : SharePoint flux de travail 2013**
      > - **Conditions : SharePoint flux de travail 2013**
  
   2. Dans le volet **Formes**, choisissez **Formes rapides**, puis faites glisser la forme de condition nommée **Si une valeur est égale à la valeur** à droite de la forme d’étape. 
    
   3. Sur l’onglet **ACCUEIL** du ruban, choisissez l’outil **Connecteur**, puis connectez la forme de sortie de l’étape à la forme de condition (voir la figure 19). 
    
      **Figure 19. Connexion d’une forme d’étape à une forme de condition dans un diagramme de flux de travail Visio**

      ![Création d’un diagramme de flux de travail dans Visio](media/pj15_CreateWorkflowSPD_NewVisioWorkflow.gif "Création d’un diagramme de flux de travail dans Visio")
  
   4. Faites glisser deux autres formes d’étape à droite de la forme de condition. Les formes sont nommées **Étape 2** et **Étape 3**.
    
   5. À l’aide de l’outil **Connecteur**, connectez le côté droit de la forme de condition à la forme d’entrée de **Étape 2**. Choisissez **l’outil Pointeur** , double-cliquez sur la connexion pour afficher une boîte de texte pour le nom, puis nommez la connexion Oui.
    
   6. Connectez le bas de la forme de condition à la forme d’entrée de **Étape 3**. À l’aide de l’outil **Pointeur**, cliquez avec le bouton droit de la souris sur la connexion, puis choisissez **Non**. Chacune de ces méthodes fonctionne pour nommer les connecteurs **Oui** ou **Non**.
    
   7. Dans le  volet Formes, choisissez **Actions - flux de travail SharePoint 2013**, puis faites glisser l’action  d’événement de projet Attendre au milieu de la forme pour l’étape **1** (voir figure 20). 
    
      **Figure 20. Réalisation du flux de travail dans Visio**

      ![Fin du flux de travail dans Visio](media/pj15_CreateWorkflowSPD_CompletedVisioWorkflow.gif "Fin du flux de travail dans Visio")
  
   8. Dans l’onglet **PROCESSUS** du ruban, dans le groupe **Validation de diagramme**, sélectionnez **Vérifier le diagramme**. Corrigez les erreurs éventuelles, puis enregistrez le dessin. Par exemple, nommez le fichier  Flux de travail de test à partir de Visio.vsdx.
    
      Pour plus d’informations sur la résolution des erreurs de flux de travail, voir [Troubleshooting SharePoint Server 2013 workflow validation errors in Visio 2013](https://msdn.microsoft.com/library/jj163971%28v=office.15%29.aspx).
    
2. Ouvrez SharePoint Designer 2013, puis ouvrez le même site Project Web App que celui que vous avez utilisé pour l’exemple de flux de travail **de** branchement. 
    
3. Choisissez **Flux de travail** dans le volet **Navigation**, puis créez un flux de travail de site (choisissez **Flux de travail de site** sur l’onglet **FLUX DE TRAVAIL** du ruban). Par exemple, nommez le flux de travail Flux de travail simple à partir de Visio.
    
   Dans la **boîte de dialogue** Créer un flux de travail de site, assurez-vous que le type de plateforme est SharePoint Flux de travail **2013 - Project Server**. Choisissez **Créer** et SharePoint concepteur ouvre le volet Concepteur texte pour le  nouveau flux de travail. 
    
4. Dans le groupe **Gérer**, sur l’onglet **FLUX DE TRAVAIL** du ruban, choisissez **Paramètres du flux de travail**.
    
5. Dans le groupe **Gérer**, sur l’onglet **PARAMÈTRES DU FLUX DE TRAVAIL** du ruban, choisissez **Importer à partir de Visio**, puis importez le fichier **Flux de travail de test à partir de Visio.vsdx** que vous avez enregistré auparavant. La boîte de dialogue **Microsoft SharePoint Designer** vous avertit que le diagramme que vous importez ne contient pas de propriétés de flux de travail et vous demande si vous voulez remplacer le flux de travail actuel. Choisissez **Oui** ; SharePoint Designer importe le diagramme de flux de travail, génère des gabarits pour les formes et affiche le volet Concepteur  visuel qui contient le flux de travail importé. 
    
6. Définissez les propriétés de chaque forme d’étape du flux de travail. Par exemple, la première forme de phase est nommée Étape **1 (** non valide) car elle ne représente pas une étape valide dans l’instance Project Web App connectée. Lorsque vous sélectionnez l’étape ou passez votre curseur dessus, vous pouvez choisir l’icône **Propriétés** en bas à gauche de la forme d’étape afin d’afficher la boîte de dialogue **Propriétés de l’étape** (voir la figure 21). Sélectionnez l’étape **Détails de la proposition initiale** dans la liste déroulante **Phase de projet**, puis cliquez sur **OK**. SharePoint designer renomme l’étape.
    
   **Figure 21. Définition des propriétés de l’étape dans SharePoint Designer**

   ![Définition des propriétés dans un flux de travail importé](media/pj15_CreateWorkflowSPD_ImportFromVisio1.gif "Définition des propriétés dans un flux de travail importé")
  
   Pour la deuxième étape, définissez la propriété **Phase de projet** sur **Refus automatique**. Pour la troisième étape, définissez la propriété **Phase de projet** sur **Exécution**.
    
7. De même, pour l’action **Attendre un événement de projet**, définissez la propriété **Nom de l’événement** sur **Événement : lors de la soumission d’un projet**.
    
8. De même, définissez les propriétés de la condition **Si une valeur est égale à la valeur**. Par exemple, définissez la première propriété **Valeur** sur **Données Projet : Coût de la proposition**. Définissez la propriété **Opérateur** sur **est inférieur à**. Définissez la deuxième **propriété Value** sur 5 000.
    
9. Vérifiez que le flux de travail ne comporte pas d’erreur, puis enregistrez-le. Si aucune erreur n’est détectée, vous pouvez passer à la vue du **Concepteur texte** (voir la figure 22). 
    
   **Figure 22. Affichage du flux de travail importé dans le Concepteur texte**

   ![Affichage du flux de travail importé](media/pj15_CreateWorkflowSPD_WorkflowFromVisio.gif "Affichage du flux de travail importé")
  
10. Publiez le flux de travail. Si vous enregistrez le flux de travail, mais que vous ne le publiez pas, il ne sera pas disponible lorsque vous créerez un type de projet d’entreprise.
    
11. Pour tester le flux de travail simple importé à partir de **Visio** dans Project Web App, créez un EPT qui utilise le flux de travail, puis créez des projets qui utilisent le nouvel EPT comme vous  l’avez fait pour l’exemple de flux de travail de branchement. Dans ce cas, toutefois, les projets dont le coût est inférieur à 5 000 $ sont rejetés. 
    
Dans cet article, vous avez créé et testé un flux de travail de branchement simple à l’aide de SharePoint Designer 2013 pour définir directement les étapes, conditions et actions que le flux de travail utilise. Vous avez également créé un diagramme pour un flux de travail de branchement encore plus simple à l’aide Visio 2013. Vous avez importé le diagramme de flux de travail Visio dans SharePoint Designer 2013, où vous définissez les propriétés de chaque étape, condition et action à partir de la connexion avec Project Web App.
  
Visio 2013 et SharePoint Designer offrent ensemble des moyens pratiques pour les concepteurs, les responsables de projets, les développeurs de flux de travail et les testeurs de créer, partager et personnaliser des conceptions de flux de travail pour différentes installations de Project Server 2013 et Project Online. Pour les flux de travail qui nécessitent un accès par programme à Project Server que SharePoint Designer ne fournit pas, vous pouvez utiliser Visual Studio 2012 avec le modèle objet côté client (CSOM).
  
## <a name="see-also"></a>Voir aussi

- [Architecture Project Server 2013](project-server-2013-architecture.md)
- [Start: Set up and configure SharePoint 2013 Gestionnaire de flux de travail](https://msdn.microsoft.com/library/jj163276%28office.15%29.aspx)
- [Comprendre comment empaqueter et déployer des flux de travail dans SharePoint 2013](https://msdn.microsoft.com/library/jj819316%28office.15%29.aspx)
- [Flux de travail dans SharePoint 2013](https://msdn.microsoft.com/library/jj163986%28office.15%29.aspx)
- [Développement de flux de travail dans SharePoint Designer 2013 et Visio 2013](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
- [Résolution des SharePoint de validation de flux de travail Server 2013 Visio 2013](https://msdn.microsoft.com/library/jj163971%28v=office.15%29.aspx)
- [Gestion des flux de travail et de la demande](https://msdn.microsoft.com/library/cf7433a3-a531-4467-ac0c-df0c5d6881ae%28Office.15%29.aspx)

