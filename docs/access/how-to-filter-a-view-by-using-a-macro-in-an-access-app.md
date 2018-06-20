---
title: Filtrer une vue à l’aide d’une macro dans une application Access
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: db4dbb71-1b22-4dfd-bc07-5f7d694fc038
description: Apprenez à filtrer une vue dans une application Access à l’aide de l’action de macro RequeryRecords et une macro de données.
ms.openlocfilehash: 9cd8c74b3949a0bb496798df663b1b42fb2868d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781867"
---
# <a name="filter-a-view-by-using-a-macro-in-an-access-app"></a><span data-ttu-id="2199b-103">Filtrer une vue à l’aide d’une macro dans une application Access</span><span class="sxs-lookup"><span data-stu-id="2199b-103">Filter a view by using a macro in an Access app</span></span>

<span data-ttu-id="2199b-104">Apprenez à filtrer une vue dans une application Access à l’aide de l’action de macro RequeryRecords et une macro de données.</span><span class="sxs-lookup"><span data-stu-id="2199b-104">Learn how to filter a view in an Access app by using the RequeryRecords macro action and a data macro.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="2199b-p101">[!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="2199b-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 

<span data-ttu-id="2199b-107">L’affichage de liste par défaut dans une application Access vous permet de filtrer les problèmes sur les valeurs contenues dans les champs.</span><span class="sxs-lookup"><span data-stu-id="2199b-107">The default list view in an Access app enables you to filter the issues on values that are contained in the fields.</span></span> <span data-ttu-id="2199b-108">Il peut arriver dans lequel vous souhaitez filtrer une vue basée sur un ensemble de conditions plutôt qu’en correspondance d’une valeur.</span><span class="sxs-lookup"><span data-stu-id="2199b-108">There may be instances where you'd like to filter a view based on a set of conditions instead of by matching a value.</span></span> <span data-ttu-id="2199b-109">Pour faire que vous devez créer une macro.</span><span class="sxs-lookup"><span data-stu-id="2199b-109">To do that you must create a macro.</span></span> <span data-ttu-id="2199b-110">Cet article vous montre comment créer une macro qui filtrer une vue pour afficher les tâches qui ont dépassé une échéance ou d’échéance dans les 7 prochains jours.</span><span class="sxs-lookup"><span data-stu-id="2199b-110">This article shows you how to create a macro that filter a view to display tasks that are past due or due in the next 7 days.</span></span>
  
## <a name="prerequisites-for-building-an-app-with-access"></a><span data-ttu-id="2199b-111">Conditions requises pour la création d’une application avec Access</span><span class="sxs-lookup"><span data-stu-id="2199b-111">Prerequisites for building an app with Access</span></span>
<span data-ttu-id="2199b-112"><a name="Access2013FilterViewByUsingMacro_Prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="2199b-112"></span></span>

<span data-ttu-id="2199b-113">Pour suivre les étapes décrites dans cet exemple, vous devez :</span><span class="sxs-lookup"><span data-stu-id="2199b-113">To follow the steps in this example, you need:</span></span>
  
- <span data-ttu-id="2199b-114">Access 2013</span><span class="sxs-lookup"><span data-stu-id="2199b-114">Access 2013</span></span>
- <span data-ttu-id="2199b-115">Un environnement de développement SharePoint 2013</span><span class="sxs-lookup"><span data-stu-id="2199b-115">A SharePoint 2013 development environment</span></span>
    
> [!NOTE]
> <span data-ttu-id="2199b-116">Pour plus d'informations sur la configuration de votre environnement de développement SharePoint, consultez [Configurer un environnement de développement général pour SharePoint 2013](http://msdn.microsoft.com/library/08e4e4e1-d960-43fa-85df-f3c279ed6927%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="2199b-116">For more information about setting up your SharePoint development environment, see [Set up a general development environment for SharePoint 2013](http://msdn.microsoft.com/library/08e4e4e1-d960-43fa-85df-f3c279ed6927%28Office.15%29.aspx).</span></span> <span data-ttu-id="2199b-117">> Pour plus d’informations sur l’obtention d’Access 2013 et SharePoint 2013, consultez les [téléchargements](http://msdn.microsoft.com/en-US/office/apps/fp123627).</span><span class="sxs-lookup"><span data-stu-id="2199b-117">>  For more information about obtaining Access 2013 and SharePoint 2013, see [Downloads](http://msdn.microsoft.com/en-US/office/apps/fp123627).</span></span> 
  
## <a name="create-the-app"></a><span data-ttu-id="2199b-118">Création de l'application</span><span class="sxs-lookup"><span data-stu-id="2199b-118">Create the app</span></span>
<span data-ttu-id="2199b-119"><a name="Access2013FilterViewByUsingMacro_CreateApp"> </a></span><span class="sxs-lookup"><span data-stu-id="2199b-119"></span></span>

<span data-ttu-id="2199b-120">Supposons que vous souhaitez créer une application Access qui effectue le suivi des tâches de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="2199b-120">Suppose you want to create an Access app that tracks tasks for your business.</span></span> <span data-ttu-id="2199b-121">Avant de commencer la création de tables et l’affichage, vous devez rechercher un modèle de schéma.</span><span class="sxs-lookup"><span data-stu-id="2199b-121">Before you start creating the tables and view, you should search for a schema template.</span></span>
  
### <a name="to-create-the-task-tracking-app"></a><span data-ttu-id="2199b-122">Pour créer l’application de suivi de tâches</span><span class="sxs-lookup"><span data-stu-id="2199b-122">To create the task tracking app</span></span>

1. <span data-ttu-id="2199b-123">Ouvrez Access, puis sélectionnez **Application web personnalisée**.</span><span class="sxs-lookup"><span data-stu-id="2199b-123">Open Access and choose **Custom web app**.</span></span>
    
2. <span data-ttu-id="2199b-p105">Entrez un nom et un emplacement web pour votre application. Vous pouvez également sélectionner un emplacement dans la liste **Emplacements**, puis sélectionner **Créer**.</span><span class="sxs-lookup"><span data-stu-id="2199b-p105">Enter a name and the web location for your app. You can also choose a location from the **Locations** list and choose **Create**.</span></span>
    
3. <span data-ttu-id="2199b-126">Tapez **tâches** dans la zone **Rechercher** , puis appuyez sur ENTRÉE.</span><span class="sxs-lookup"><span data-stu-id="2199b-126">Type **tasks** into the **Search** box and then press ENTER.</span></span> 
    
    <span data-ttu-id="2199b-127">Une liste de modèles qui peuvent être utiles pour le suivi des tâches s’affiche dans la Figure 1.</span><span class="sxs-lookup"><span data-stu-id="2199b-127">A list of templates that might be useful for tracking tasks is displayed in Figure 1.</span></span>
    
   <span data-ttu-id="2199b-128">**La figure 1. Modèles correspondant à la recherche de tâches**</span><span class="sxs-lookup"><span data-stu-id="2199b-128">**Figure 1. Templates that match the search for tasks**</span></span>

   <span data-ttu-id="2199b-129">![Modèles qui correspondent à la recherche de problèmes] (media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Modèles qui correspondent à la recherche de problèmes")</span><span class="sxs-lookup"><span data-stu-id="2199b-129">![Templates that match the search for issues](media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Templates that match the search for issues")</span></span>
  
4. <span data-ttu-id="2199b-130">Cliquez sur **tâches**.</span><span class="sxs-lookup"><span data-stu-id="2199b-130">Choose **Tasks**.</span></span>
    
<span data-ttu-id="2199b-131">Access crée un ensemble de tables et d'affichages.</span><span class="sxs-lookup"><span data-stu-id="2199b-131">Access creates a set of tables and views.</span></span>
  
<span data-ttu-id="2199b-132">Entrez plusieurs exemples de tâches et employés dans votre application.</span><span class="sxs-lookup"><span data-stu-id="2199b-132">Enter several sample tasks and employees in your app.</span></span> <span data-ttu-id="2199b-133">Pour ce faire, choisissez **Lancer l’application** pour ouvrir l’application dans votre navigateur web.</span><span class="sxs-lookup"><span data-stu-id="2199b-133">To do this, choose **Launch App** to open the app in your web browser.</span></span> <span data-ttu-id="2199b-134">Entrez une valeur dans le champ **Date d’échéance** pour chaque tâche.</span><span class="sxs-lookup"><span data-stu-id="2199b-134">Enter a value in the **Due Date** field for each task.</span></span> <span data-ttu-id="2199b-135">Lorsque vous avez terminé, retournez dans Access.</span><span class="sxs-lookup"><span data-stu-id="2199b-135">Return to Access when you're done.</span></span> 
  
## <a name="plan-the-customizations"></a><span data-ttu-id="2199b-136">Planifier les personnalisations</span><span class="sxs-lookup"><span data-stu-id="2199b-136">Plan the customizations</span></span>
<span data-ttu-id="2199b-137"><a name="Access2013FilterViewByUsingMacro_PlanCustomizations"> </a></span><span class="sxs-lookup"><span data-stu-id="2199b-137"></span></span>

<span data-ttu-id="2199b-138">Vous avez maintenant une application qui contient plusieurs tâches.</span><span class="sxs-lookup"><span data-stu-id="2199b-138">You now have an app that contains several tasks.</span></span> <span data-ttu-id="2199b-139">L’affichage par défaut permet de rechercher les tâches à l’aide des éléments qui sont stockés dans les champs affichés dans l’affichage.</span><span class="sxs-lookup"><span data-stu-id="2199b-139">The default view enables you to search for any tasks using items that are stored in the fields displayed in the view.</span></span> <span data-ttu-id="2199b-140">Par exemple, vous pouvez rechercher pour les problèmes de haute priorité ou en cours.</span><span class="sxs-lookup"><span data-stu-id="2199b-140">For example, you can search for high-priority issues or issues in progress.</span></span> <span data-ttu-id="2199b-141">Supposons que vous souhaitez définir la priorité de votre travail, en affichant les problèmes actifs qui arrive à échéance dans la semaine à venir.</span><span class="sxs-lookup"><span data-stu-id="2199b-141">Suppose you want to prioritize your work by displaying active issues that are due in the coming week.</span></span> <span data-ttu-id="2199b-142">Pour ce faire, vous devez créer une macro de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2199b-142">To do this, you should create a user interface (UI) macro.</span></span>
  
<span data-ttu-id="2199b-143">La commande de macro d’interface utilisateur que vous pouvez utiliser pour filtrer l’affichage est l' [Action de Macro RequeryRecords (accès web personnalisé application)](requeryrecords-macro-action-access-custom-web-app.md).</span><span class="sxs-lookup"><span data-stu-id="2199b-143">The UI macro command that you can use to filter the view is the [RequeryRecords Macro Action (Access custom web app)](requeryrecords-macro-action-access-custom-web-app.md).</span></span> <span data-ttu-id="2199b-144">L’action de macro **RequeryRecords** filtre l’affichage en fonction de l’argument *où* , qui est fourni sous la forme d’une clause WHERE SQL.</span><span class="sxs-lookup"><span data-stu-id="2199b-144">The **RequeryRecords** macro action filters the view based on the  *Where*  argument, which is provided in the form of a SQL WHERE clause.</span></span> <span data-ttu-id="2199b-145">Pour filtrer l’affichage, vous devez fournir plusieurs faits dans un format spécifique pour filtrer l’affichage.</span><span class="sxs-lookup"><span data-stu-id="2199b-145">To filter the view, you must supply several facts in a specific format to filter the view.</span></span> 
  
<span data-ttu-id="2199b-146">Les faits pertinents sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="2199b-146">The relevant facts are:</span></span>
  
- <span data-ttu-id="2199b-147">L’ou les champs à comparer</span><span class="sxs-lookup"><span data-stu-id="2199b-147">The field or fields to compare</span></span>
    
- <span data-ttu-id="2199b-148">Comment faire référence à la date du jour</span><span class="sxs-lookup"><span data-stu-id="2199b-148">How to refer to today's date</span></span>
    
- <span data-ttu-id="2199b-149">Comment faire référence à un jour donné par rapport à la date du jour</span><span class="sxs-lookup"><span data-stu-id="2199b-149">How to refer to a particular day relative to today's date</span></span>
    
- <span data-ttu-id="2199b-150">Comment déterminer lequel des tâches sont en cours</span><span class="sxs-lookup"><span data-stu-id="2199b-150">How to determine which on tasks are in progress</span></span>
    
<span data-ttu-id="2199b-151">Le champ **Date d’échéance** fournit des informations sur lorsqu’une tâche est due.</span><span class="sxs-lookup"><span data-stu-id="2199b-151">The **Due Date** field provides information about when a task is due.</span></span> <span data-ttu-id="2199b-152">Le champ **état** fournit des informations d’état relatives à chaque tâche.</span><span class="sxs-lookup"><span data-stu-id="2199b-152">The **Status** field provides status information about each task.</span></span> <span data-ttu-id="2199b-153">Pour faire référence à un champ dans une macro, utilisez le format **[*TableName*]. [ *FieldName*]**.</span><span class="sxs-lookup"><span data-stu-id="2199b-153">To refer to a field in a macro, use the format **[*TableName*].[*FieldName*]**.</span></span> <span data-ttu-id="2199b-154">Utilisez **[tâches]. [ Date d’échéance]** pour faire référence au champ **Date d’échéance** et **[tâches]. [ État]** pour faire référence au champ **d’état** .</span><span class="sxs-lookup"><span data-stu-id="2199b-154">Use **[Tasks].[Due Date]** to refer to the **Due Date** field and **[Tasks].[Status]** to refer to the **Status** field.</span></span> 
  
<span data-ttu-id="2199b-155">La fonction de la [Fonction aujourd'hui (accès personnalisé web app)](today-function-access-custom-web-app.md) renvoie la date du jour.</span><span class="sxs-lookup"><span data-stu-id="2199b-155">The [Today Function (Access custom web app)](today-function-access-custom-web-app.md) function returns today's date.</span></span> <span data-ttu-id="2199b-156">La fonction [DateAdd (accès personnalisé web app)](dateadd-function-access-custom-web-app.md) peut servir à calculer une date est un certain nombre de jours après la date spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2199b-156">The [DateAdd Function (Access custom web app)](dateadd-function-access-custom-web-app.md) function can be used to calculate a date that's a certain number of days after a specified date.</span></span> 
  
<span data-ttu-id="2199b-157">Le champ **état** contient plusieurs valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="2199b-157">The **Status** field contains several possible values.</span></span> <span data-ttu-id="2199b-158">Une valeur **terminé** indique que la tâche n’est plus active.</span><span class="sxs-lookup"><span data-stu-id="2199b-158">A value of **Completed** indicates that the task is no longer active.</span></span> 
  
<span data-ttu-id="2199b-159">Ces éléments peuvent être combinés dans la clause WHERE SQL suivante.</span><span class="sxs-lookup"><span data-stu-id="2199b-159">These facts can be combined into the following SQL WHERE clause.</span></span>
  
```sql
[Tasks].[Due Date]<DateAdd(Day,7,Today()) AND [Tasks].[Status]<>"Completed"
```

<span data-ttu-id="2199b-160">Cette clause SQL WHERE permet de filtrer l’affichage pour afficher les problèmes actifs qui arrive à échéance dans les 7 prochains jours ou retard dans la macro.</span><span class="sxs-lookup"><span data-stu-id="2199b-160">This SQL WHERE clause is used in the macro to filter the view to display active issues that are due in the next 7 days or are past due.</span></span>
  
<span data-ttu-id="2199b-161">Pour exécuter la macro d’interface utilisateur, il doit être joint à un élément ou d’un événement qui se produit dans l’affichage.</span><span class="sxs-lookup"><span data-stu-id="2199b-161">To run the UI macro, it must be attached to an item or an event that occurs in the view.</span></span> <span data-ttu-id="2199b-162">La **Barre d’Action** est un emplacement pratique pour ajouter une commande personnalisée à l’affichage.</span><span class="sxs-lookup"><span data-stu-id="2199b-162">The **Action Bar** is a convenient place to add a custom command to the view.</span></span> <span data-ttu-id="2199b-163">La **Barre d’Action** est une barre d’outils personnalisable qui s’affiche en haut de chaque mode d’affichage.</span><span class="sxs-lookup"><span data-stu-id="2199b-163">The **Action Bar** is a customizable toolbar that appears at the top of each view.</span></span> <span data-ttu-id="2199b-164">Par défaut, la **Barre d’Action** contient des boutons pour ajouter, modifier, enregistrer, supprimer et annuler les modifications.</span><span class="sxs-lookup"><span data-stu-id="2199b-164">By default, the **Action Bar** contains buttons to add, edit, save, delete, and cancel edits.</span></span> <span data-ttu-id="2199b-165">Vous pouvez ajouter des boutons qui exécutent des actions personnalisées, telles que le filtrage de la vue.</span><span class="sxs-lookup"><span data-stu-id="2199b-165">You can add buttons that perform custom actions, such as filtering the view.</span></span> 
  
<span data-ttu-id="2199b-166">Si l’affichage contient les enregistrements qui répondent aux critères spécifiés, **RequeryRecords** filtre l’affichage.</span><span class="sxs-lookup"><span data-stu-id="2199b-166">If the view contains records that meet the specified criteria, then **RequeryRecords** filters the view.</span></span> <span data-ttu-id="2199b-167">Toutefois, si l’affichage ne contient pas tous les enregistrements qui répondent aux critères, à un nouvel enregistrement vide s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2199b-167">However, if the view doesn't contain any records that meet the criteria, than a new, blank record is displayed.</span></span> <span data-ttu-id="2199b-168">Si vous ne souhaitez pas un enregistrement vide s’affiche si aucune tâche n’est due la semaine suivante, vous devez trouver une méthode pour vérifier les tâches avant d’appeler l’action de macro **RequeryRecords** .</span><span class="sxs-lookup"><span data-stu-id="2199b-168">If you don't want a blank record to be displayed if no tasks are due in the next week, then you must find a method to check the tasks before you call the **RequeryRecords** macro action.</span></span> <span data-ttu-id="2199b-169">Pour ce faire, créez une macro de données pour vérifier les enregistrements qui répondent aux critères.</span><span class="sxs-lookup"><span data-stu-id="2199b-169">To do this, create a data macro to check for records that meet the criteria.</span></span> 
  
<span data-ttu-id="2199b-170">La macro d’interface utilisateur appelle la macro de données, qui tente de trouver une tâche due la semaine prochaine.</span><span class="sxs-lookup"><span data-stu-id="2199b-170">The UI macro will call the data macro, which will try to find a task that's due in the next week.</span></span> <span data-ttu-id="2199b-171">Si la macro de données détecte la tâche, puis personnaliser l’application.</span><span class="sxs-lookup"><span data-stu-id="2199b-171">If the data macro finds the task then customize the app.</span></span>
  
## <a name="customize-the-app"></a><span data-ttu-id="2199b-172">Personnalisation de l'application</span><span class="sxs-lookup"><span data-stu-id="2199b-172">Customize the app</span></span>
<span data-ttu-id="2199b-173"><a name="Access2013FilterViewByUsingMacro_CustomizeApp"> </a></span><span class="sxs-lookup"><span data-stu-id="2199b-173"></span></span>

<span data-ttu-id="2199b-174">Maintenant que vous avez déterminé les personnalisations, les implémenter.</span><span class="sxs-lookup"><span data-stu-id="2199b-174">Now that you've determined the customizations, implement them.</span></span> <span data-ttu-id="2199b-175">La macro de données doit être créée en premier.</span><span class="sxs-lookup"><span data-stu-id="2199b-175">The data macro should be created first.</span></span> <span data-ttu-id="2199b-176">Certaines macros de données sont connectées directement à des tables.</span><span class="sxs-lookup"><span data-stu-id="2199b-176">Some data macros are attached directly to tables.</span></span> <span data-ttu-id="2199b-177">Toutefois, cette macro de données est une macro de données autonome.</span><span class="sxs-lookup"><span data-stu-id="2199b-177">However, this data macro is a stand-alone data macro.</span></span>
  
### <a name="to-create-the-data-macro"></a><span data-ttu-id="2199b-178">Pour créer la macro de données</span><span class="sxs-lookup"><span data-stu-id="2199b-178">To create the data macro</span></span>

1. <span data-ttu-id="2199b-179">Ouvrez l'application dans Access.</span><span class="sxs-lookup"><span data-stu-id="2199b-179">Open the app in Access.</span></span>
    
2. <span data-ttu-id="2199b-180">Dans le groupe **Créer**, sélectionnez **Avancé**, puis **Macro de données**.</span><span class="sxs-lookup"><span data-stu-id="2199b-180">In the **Create** group, choose **Advanced**, and then choose **Data Macro**.</span></span>
    
    <span data-ttu-id="2199b-181">Une macro de données vide s’ouvre en mode Création de macro.</span><span class="sxs-lookup"><span data-stu-id="2199b-181">A blank data macro is opened in macro Design View.</span></span>
    
3. <span data-ttu-id="2199b-182">Dans la zone de liste **Ajouter une nouvelle Action** , sélectionnez **RechercherEnregistrement**.</span><span class="sxs-lookup"><span data-stu-id="2199b-182">From the **Add New Action** list box, choose **LookupRecord**.</span></span>
    
4. <span data-ttu-id="2199b-183">Dans la zone de liste **Rechercher un enregistrement dans** , sélectionnez **tâches**.</span><span class="sxs-lookup"><span data-stu-id="2199b-183">In the **Look Up A Record In** list box, choose **Tasks**.</span></span>
    
5. <span data-ttu-id="2199b-184">Dans la zone **Condition Where** , entrez **[tâches]. [ Date d’échéance]\<DateAdd(Day,7,Today()) et [tâches]. [État] \< \>« Completed »**.</span><span class="sxs-lookup"><span data-stu-id="2199b-184">In the **Where Condition** box, enter **[Tasks].[Due Date]\<DateAdd(Day,7,Today()) AND [Tasks].[Status]\<\>"Completed"**.</span></span> 
    
6. <span data-ttu-id="2199b-185">Dans la liste déroulante **Ajouter une nouvelle Action** , sélectionnez **SetReturnVar** .</span><span class="sxs-lookup"><span data-stu-id="2199b-185">Choose **SetReturnVar** from the **Add New Action** list box.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="2199b-186">Vous verrez deux zones de liste **Ajouter une nouvelle Action** , un dans le bloc **RechercherEnregistrement** et l’autre en dehors du bloc **RechercherEnregistrement** .</span><span class="sxs-lookup"><span data-stu-id="2199b-186">You'll see two **Add New Action** list boxes, one within the **LookupRecord** block, and another outside the **LookupRecord** block.</span></span> <span data-ttu-id="2199b-187">Vous devez choisir la zone de liste **Ajouter une nouvelle Action** dans le bloc **RechercherEnregistrement** , comme le montre la Figure 1.</span><span class="sxs-lookup"><span data-stu-id="2199b-187">You should choose the **Add New Action** list box within the **LookupRecord** block, as shown in Figure 1.</span></span> 
  
   <span data-ttu-id="2199b-188">**La figure 1. Ajouter la zone de liste d’une nouvelle Action**</span><span class="sxs-lookup"><span data-stu-id="2199b-188">**Figure 1. Add New Action list box**</span></span>

   <span data-ttu-id="2199b-189">![Liste déroulante Ajouter une nouvelle Action] (media/odc_Access2013_FilterFormByUsingMacro_Figure01.jpg "Liste déroulante Ajouter une nouvelle Action")</span><span class="sxs-lookup"><span data-stu-id="2199b-189">![Add New Action dropdown](media/odc_Access2013_FilterFormByUsingMacro_Figure01.jpg "Add New Action dropdown")</span></span>
  
7. <span data-ttu-id="2199b-190">Dans la zone **nom** , entrez **TaskFound**.</span><span class="sxs-lookup"><span data-stu-id="2199b-190">In the **Name** box, enter **TaskFound**.</span></span> 
    
8. <span data-ttu-id="2199b-191">Dans la zone **Expression** , entrez **« Oui »**.</span><span class="sxs-lookup"><span data-stu-id="2199b-191">In the **Expression** box, enter **"Yes"**.</span></span> 
    
9. <span data-ttu-id="2199b-192">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2199b-192">Choose **Save**.</span></span> <span data-ttu-id="2199b-193">Entrez **TasksDueSoon** dans la zone **Nom de la Macro** , puis choisissez **OK**.</span><span class="sxs-lookup"><span data-stu-id="2199b-193">Enter **TasksDueSoon** in the **Macro Name** box and then choose **OK**.</span></span>
    
    <span data-ttu-id="2199b-194">La macro doit ressembler celle illustrée à la Figure 2.</span><span class="sxs-lookup"><span data-stu-id="2199b-194">The macro should resemble the macro shown in Figure 2.</span></span>
    
   <span data-ttu-id="2199b-195">**La figure 2. Macro de données TasksDueSoon**</span><span class="sxs-lookup"><span data-stu-id="2199b-195">**Figure 2. TasksDueSoon data macro**</span></span>

   <span data-ttu-id="2199b-196">![Macro de données TasksDueSoon] (media/odc_Access2013_FilterFormByUsingMacro_Figure02.jpg "Macro de données TasksDueSoon")</span><span class="sxs-lookup"><span data-stu-id="2199b-196">![TasksDueSoon data macro](media/odc_Access2013_FilterFormByUsingMacro_Figure02.jpg "TasksDueSoon data macro")</span></span>
  
10. <span data-ttu-id="2199b-197">Fermez l'affichage Création de macros.</span><span class="sxs-lookup"><span data-stu-id="2199b-197">Close macro Design View.</span></span>
    
<span data-ttu-id="2199b-198">À présent, nous sommes prêts à ajouter un bouton personnalisé à la barre d’Action.</span><span class="sxs-lookup"><span data-stu-id="2199b-198">Now, we're ready to add a custom button to the Action Bar.</span></span>
  
### <a name="to-add-a-custom-button-to-the-action-bar"></a><span data-ttu-id="2199b-199">Pour ajouter un bouton personnalisé à la barre d’Action</span><span class="sxs-lookup"><span data-stu-id="2199b-199">To add a custom button to the Action Bar</span></span>

1. <span data-ttu-id="2199b-200">Choisissez le tableau des **tâches** .</span><span class="sxs-lookup"><span data-stu-id="2199b-200">Choose the **Tasks** table.</span></span> <span data-ttu-id="2199b-201">Il choisit le formulaire de liste de tâches.</span><span class="sxs-lookup"><span data-stu-id="2199b-201">This chooses the Tasks List form.</span></span> 
    
2. <span data-ttu-id="2199b-202">Dans le sélecteur d'affichage, sélectionnez **Liste**, l'icône **Paramètres/Action**, puis **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="2199b-202">In the View selector, choose **List**, choose the **Settings/Action** icon, and then choose **Edit**.</span></span>
    
    <span data-ttu-id="2199b-203">L’affichage est ouvert en mode Création.</span><span class="sxs-lookup"><span data-stu-id="2199b-203">The view is opened in Design View.</span></span>
    
3. <span data-ttu-id="2199b-204">À présent, nous sommes prêts à ajouter un bouton personnalisé à la barre d’Action.</span><span class="sxs-lookup"><span data-stu-id="2199b-204">Now, we're ready to add a custom button to the Action Bar.</span></span> <span data-ttu-id="2199b-205">Pour ce faire, choisissez **Ajouter une action personnalisée** , comme indiqué dans la Figure 3.</span><span class="sxs-lookup"><span data-stu-id="2199b-205">To do this, choose **Add custom action** as shown in Figure 3.</span></span> 
    
   <span data-ttu-id="2199b-206">**La figure 3. Ajouter le bouton d’action personnalisée**</span><span class="sxs-lookup"><span data-stu-id="2199b-206">**Figure 3. Add custom action button**</span></span>

   <span data-ttu-id="2199b-207">![Bouton Ajoutez une action personnalisée] (media/odc_Access2013_FilterFormByUsingMacro_Figure03.jpg "Bouton Ajoutez une action personnalisée")</span><span class="sxs-lookup"><span data-stu-id="2199b-207">![Add custom action button](media/odc_Access2013_FilterFormByUsingMacro_Figure03.jpg "Add custom action button")</span></span>
  
    <span data-ttu-id="2199b-208">La nouvelle action est affichée comme un bouton avec une icône en étoile, comme le montre la Figure 4.</span><span class="sxs-lookup"><span data-stu-id="2199b-208">The new action is displayed as a button with a star icon as shown in Figure 4.</span></span>
    
   <span data-ttu-id="2199b-209">**La figure 4. Nouveau bouton de barre d’Action**</span><span class="sxs-lookup"><span data-stu-id="2199b-209">**Figure 4. New Action Bar button**</span></span>

   <span data-ttu-id="2199b-210">![Bouton nouvelle barre d’Action] (media/odc_Access2013_FilterFormByUsingMacro_Figure04.jpg "Bouton nouvelle barre d’Action")</span><span class="sxs-lookup"><span data-stu-id="2199b-210">![New Action Bar button](media/odc_Access2013_FilterFormByUsingMacro_Figure04.jpg "New Action Bar button")</span></span>
  
4. <span data-ttu-id="2199b-211">Cliquez sur le bouton de barre d’Action personnalisée, puis cliquez sur l’icône de **données** .</span><span class="sxs-lookup"><span data-stu-id="2199b-211">Choose the custom Action Bar Button, and then choose the **Data** icon.</span></span> 
    
    <span data-ttu-id="2199b-212">La boîte de dialogue **données** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2199b-212">The **Data** dialog box appears.</span></span> 
    
5. <span data-ttu-id="2199b-213">Dans la zone **Nom du contrôle** , entrez **FilterTasks**.</span><span class="sxs-lookup"><span data-stu-id="2199b-213">In the **Control Name** box, enter **FilterTasks**.</span></span> 
    
6. <span data-ttu-id="2199b-214">Dans la zone **info-bulle** , entrez **l’affichage tâches au-delà d’échéance ou d’échéance de la semaine suivante**.</span><span class="sxs-lookup"><span data-stu-id="2199b-214">In the **Tooltip** box, enter **Display tasks past due or due in the next week**.</span></span> 
    
<span data-ttu-id="2199b-215">À présent, nous sommes prêts à créer la macro d’interface utilisateur qui filtre l’affichage.</span><span class="sxs-lookup"><span data-stu-id="2199b-215">Now, we're ready to create the UI macro that will filter the view.</span></span>
  
### <a name="to-create-the-ui-macro-to-filter-the-view"></a><span data-ttu-id="2199b-216">Pour créer la macro d’interface utilisateur pour filtrer l’affichage</span><span class="sxs-lookup"><span data-stu-id="2199b-216">To create the UI macro to filter the view</span></span>

1. <span data-ttu-id="2199b-217">Dans la boîte de dialogue **données** , choisissez **En cliquant sur** comme indiqué dans la Figure 5.</span><span class="sxs-lookup"><span data-stu-id="2199b-217">In the **Data** dialog box, choose **On Click** as shown in Figure 5.</span></span> 
    
   <span data-ttu-id="2199b-218">**La figure 5. Boîte de dialogue données**</span><span class="sxs-lookup"><span data-stu-id="2199b-218">**Figure 5. Data dialog box**</span></span>

   <span data-ttu-id="2199b-219">![Boîte de dialogue données] (media/odc_Access2013_FilterFormByUsingMacro_Figure05.jpg "Boîte de dialogue données")</span><span class="sxs-lookup"><span data-stu-id="2199b-219">![Data dialog box](media/odc_Access2013_FilterFormByUsingMacro_Figure05.jpg "Data dialog box")</span></span>
  
    <span data-ttu-id="2199b-220">Une macro d’interface utilisateur vide est ouvert en mode Création de macro.</span><span class="sxs-lookup"><span data-stu-id="2199b-220">A blank UI macro is opened in macro Design View.</span></span>
    
2. <span data-ttu-id="2199b-221">Dans la liste **Ajouter une nouvelle Action** , sélectionnez **ExécuterMacroDonnées**.</span><span class="sxs-lookup"><span data-stu-id="2199b-221">From the **Add New Action** list box, choose **RunDataMacro**.</span></span> 
    
3. <span data-ttu-id="2199b-222">Dans la zone Nom de la Macro, entrez **TasksDueSoon**.</span><span class="sxs-lookup"><span data-stu-id="2199b-222">In the Macro Name box, enter **TasksDueSoon**.</span></span> 
    
    <span data-ttu-id="2199b-223">Dans le champ **DéfinirVarLocale** , entrez **FilterRecords**.</span><span class="sxs-lookup"><span data-stu-id="2199b-223">In the **SetLocalVar** box, enter **FilterRecords**.</span></span> 
    
    <span data-ttu-id="2199b-224">L’action **ExécuterMacroDonnées** appelle la macro de données **TasksDueSoon** créés précédemment et stocke le résultat dans une variable nommée **FilterRecords**.</span><span class="sxs-lookup"><span data-stu-id="2199b-224">The **RunDataMacro** action calls the **TasksDueSoon** data macro we created earlier and stores its result in a variable named **FilterRecords**.</span></span> 
    
4. <span data-ttu-id="2199b-225">Dans la zone de liste **Ajouter une nouvelle Action** , choisissez **Si**.</span><span class="sxs-lookup"><span data-stu-id="2199b-225">From the **Add New Action** list box, choose **If**.</span></span> 
    
5. <span data-ttu-id="2199b-226">Dans la zone **Si** , entrez **[FilterRecords] = « Yes »**.</span><span class="sxs-lookup"><span data-stu-id="2199b-226">In the **If** box, enter **[FilterRecords]="Yes"**.</span></span> 
    
6. <span data-ttu-id="2199b-227">Dans la zone de liste **Ajouter une nouvelle Action** , choisissez **RequeryRecords**.</span><span class="sxs-lookup"><span data-stu-id="2199b-227">From the **Add New Action** list box, choose **RequeryRecords**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="2199b-228">Vous verrez deux zones de liste **Ajouter une nouvelle Action** , un dans le bloc **If** et une autre à l’extérieur du bloc **If** .</span><span class="sxs-lookup"><span data-stu-id="2199b-228">You'll see two **Add New Action** list boxes, one within the **If** block, and another outside the **If** block.</span></span> <span data-ttu-id="2199b-229">Vous devez choisir la zone de liste **Ajouter une nouvelle Action** dans le bloc **If** , comme le montre la Figure 6.</span><span class="sxs-lookup"><span data-stu-id="2199b-229">You should choose the **Add New Action** list box within the **If** block, as shown in Figure 6.</span></span> 
  
   <span data-ttu-id="2199b-230">**La figure 6. Ajouter la zone de liste d’une nouvelle Action**</span><span class="sxs-lookup"><span data-stu-id="2199b-230">**Figure 6. Add New Action list box**</span></span>

   <span data-ttu-id="2199b-231">![Liste déroulante Ajouter une nouvelle Action] (media/odc_Access2013_FilterFormByUsingMacro_Figure06.jpg "Liste déroulante Ajouter une nouvelle Action")</span><span class="sxs-lookup"><span data-stu-id="2199b-231">![Add New Action dropdown](media/odc_Access2013_FilterFormByUsingMacro_Figure06.jpg "Add New Action dropdown")</span></span>
  
7. <span data-ttu-id="2199b-232">Dans la zone **où** , entrez **[tâches]. [ Date d’échéance]\<DateAdd(Day,7,Today()) et [tâches]. [État] \< \>« Completed »**.</span><span class="sxs-lookup"><span data-stu-id="2199b-232">In the **Where** box, enter **[Tasks].[Due Date]\<DateAdd(Day,7,Today()) AND [Tasks].[Status]\<\>"Completed"**.</span></span> 
    
8. <span data-ttu-id="2199b-233">Dans la zone **Order By** , entrez **[Date d’échéance]**.</span><span class="sxs-lookup"><span data-stu-id="2199b-233">In the **Order By** box, enter **[Due Date]**.</span></span> 
    
9. <span data-ttu-id="2199b-234">Cliquez sur le lien **Ajouter un autre** qui s’affiche à droite de la zone **Ajouter une nouvelle Action** , comme le montre la Figure 7.</span><span class="sxs-lookup"><span data-stu-id="2199b-234">Choose the **Add Else** link that appears to the right side of the **Add New Action** box as shown in Figure 7.</span></span> 
    
   <span data-ttu-id="2199b-235">**La figure 7. Lien Ajouter Sinon**</span><span class="sxs-lookup"><span data-stu-id="2199b-235">**Figure 7. Add Else link**</span></span>

   <span data-ttu-id="2199b-236">![Ajouter un autre lien] (media/odc_Access2013_FilterFormByUsingMacro_Figure07.jpg "Ajouter un autre lien")</span><span class="sxs-lookup"><span data-stu-id="2199b-236">![Add Else link](media/odc_Access2013_FilterFormByUsingMacro_Figure07.jpg "Add Else link")</span></span>
  
    <span data-ttu-id="2199b-237">Une clause Else est ajoutée au si bloc.</span><span class="sxs-lookup"><span data-stu-id="2199b-237">An Else clause is added to the If block.</span></span>
    
10. <span data-ttu-id="2199b-238">Dans la zone de liste **Ajouter une nouvelle Action** , choisissez **contrôle zonemessage.**.</span><span class="sxs-lookup"><span data-stu-id="2199b-238">From the **Add New Action** list box, choose **MessageBox**.</span></span> 
    
11. <span data-ttu-id="2199b-239">Dans la boîte de **Message** , entrez **aucune tâche n’est en retard ou arrivant à échéance dans les 7 prochains jours !**.</span><span class="sxs-lookup"><span data-stu-id="2199b-239">In the **Message** box, enter **No tasks are overdue or due in the next 7 days!**.</span></span> 
    
12. <span data-ttu-id="2199b-240">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2199b-240">Choose **Save**.</span></span>
    
    <span data-ttu-id="2199b-241">La macro doit ressembler celle illustrée à la figure 8.</span><span class="sxs-lookup"><span data-stu-id="2199b-241">The macro should resemble the macro shown in Figure 8.</span></span>
    
    <span data-ttu-id="2199b-242">**La figure 8. Macro d’interface utilisateur pour filtrer l’affichage**</span><span class="sxs-lookup"><span data-stu-id="2199b-242">**Figure 8. UI macro to filter the view**</span></span>

    <span data-ttu-id="2199b-243">![Macro d’interface utilisateur pour filtrer l’affichage] (media/odc_Access2013_FilterFormByUsingMacro_Figure08.jpg "Macro d’interface utilisateur pour filtrer l’affichage")</span><span class="sxs-lookup"><span data-stu-id="2199b-243">![UI macro to filter the view](media/odc_Access2013_FilterFormByUsingMacro_Figure08.jpg "UI macro to filter the view")</span></span>
  
13. <span data-ttu-id="2199b-244">Fermez l'affichage Création de macros.</span><span class="sxs-lookup"><span data-stu-id="2199b-244">Close macro Design View.</span></span>
    
<span data-ttu-id="2199b-245">À ce stade, nous avons créé la macro d’interface utilisateur qui permet de filtrer l’affichage de liste de tâches pour afficher les tâches urgentes.</span><span class="sxs-lookup"><span data-stu-id="2199b-245">At this point, we've created the UI macro that filters the Tasks List view to display the urgent tasks.</span></span> <span data-ttu-id="2199b-246">Il n’est pas poli laisser l’affichage dans un état filtré sans fournir une méthode pour supprimer le filtre.</span><span class="sxs-lookup"><span data-stu-id="2199b-246">It wouldn't be polite to leave the view in a filtered state without providing a method to remove the filter.</span></span> <span data-ttu-id="2199b-247">Pour ce faire, ajoutez un autre bouton de barre d’Action et Macro d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2199b-247">To do this, add another Action Bar button and UI Macro.</span></span>
  
### <a name="to-add-an-action-bar-button-to-remove-the-filter"></a><span data-ttu-id="2199b-248">Pour ajouter un bouton de barre d’Action pour supprimer le filtre</span><span class="sxs-lookup"><span data-stu-id="2199b-248">To add an Action Bar Button to remove the filter</span></span>

1. <span data-ttu-id="2199b-249">Choisissez **Ajouter une action personnalisée**.</span><span class="sxs-lookup"><span data-stu-id="2199b-249">Choose **Add custom action**.</span></span>
    
    <span data-ttu-id="2199b-250">La nouvelle action est affichée comme un bouton avec une icône en étoile</span><span class="sxs-lookup"><span data-stu-id="2199b-250">The new action is displayed as a button with a star icon</span></span>
    
2. <span data-ttu-id="2199b-251">Cliquez sur le bouton de barre d’Action personnalisé, puis cliquez sur l’icône de **données** .</span><span class="sxs-lookup"><span data-stu-id="2199b-251">Choose the custom Action Bar button, and then choose the **Data** icon.</span></span> 
    
    <span data-ttu-id="2199b-252">La boîte de dialogue **données** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2199b-252">The **Data** dialog box appears.</span></span> 
    
3. <span data-ttu-id="2199b-253">Dans la zone **Nom du contrôle** , entrez **RemoveFilter**.</span><span class="sxs-lookup"><span data-stu-id="2199b-253">In the **Control Name** box, enter **RemoveFilter**.</span></span> 
    
4. <span data-ttu-id="2199b-254">Dans la zone **info-bulle** , entrez **Supprimer tous les filtres appliqués à l’affichage**.</span><span class="sxs-lookup"><span data-stu-id="2199b-254">In the **Tooltip** box, enter **Remove all filter applied to the view**.</span></span> 
    
<span data-ttu-id="2199b-255">À présent, nous sommes prêts à créer la macro d’interface utilisateur qui permet de supprimer le filtre l’affichage.</span><span class="sxs-lookup"><span data-stu-id="2199b-255">Now, we're ready to create the UI macro that will remove the filter form the view.</span></span>
  
### <a name="to-create-the-ui-macro-to-remove-the-filter-from-the-view"></a><span data-ttu-id="2199b-256">Pour créer la macro d’interface utilisateur pour supprimer le filtre de l’affichage</span><span class="sxs-lookup"><span data-stu-id="2199b-256">To create the UI macro to remove the filter from the view</span></span>

1. <span data-ttu-id="2199b-257">Dans la boîte de dialogue **données** , choisissez **En cliquant sur**.</span><span class="sxs-lookup"><span data-stu-id="2199b-257">In the **Data** dialog box, choose **On Click**.</span></span>
    
    <span data-ttu-id="2199b-258">Une macro d’interface utilisateur vide est ouvert en mode Création de macro.</span><span class="sxs-lookup"><span data-stu-id="2199b-258">A blank UI macro is opened in macro Design View.</span></span>
    
2. <span data-ttu-id="2199b-259">Dans la zone de liste **Ajouter une nouvelle Action** , choisissez **RequeryRecords**.</span><span class="sxs-lookup"><span data-stu-id="2199b-259">From the **Add New Action** list box, choose **RequeryRecords**.</span></span> 
    
    <span data-ttu-id="2199b-260">Cette fois-ci, nous allons laissez les zones **où** et **Order By** vide.</span><span class="sxs-lookup"><span data-stu-id="2199b-260">This time, we'll leave the **Where** and **Order By** boxes empty.</span></span> <span data-ttu-id="2199b-261">L’action **RequeryRecords** est appelée sans aucun paramètre, tous les filtres sont supprimés de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="2199b-261">Then the **RequeryRecords** action is called without any parameters, all filters are removed from the view.</span></span> 
    
3. <span data-ttu-id="2199b-262">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2199b-262">Choose **Save**.</span></span>
    
4. <span data-ttu-id="2199b-263">Fermez l'affichage Création de macros.</span><span class="sxs-lookup"><span data-stu-id="2199b-263">Close macro Design View.</span></span>
    
5. <span data-ttu-id="2199b-264">Fermez l’affichage de liste de tâches.</span><span class="sxs-lookup"><span data-stu-id="2199b-264">Close the Tasks List view.</span></span> <span data-ttu-id="2199b-265">Lorsque vous êtes invité à enregistrer vos modifications, sélectionnez **Oui**.</span><span class="sxs-lookup"><span data-stu-id="2199b-265">Choose **Yes** when you are prompted to save your changes.</span></span> 
    
<span data-ttu-id="2199b-266">À présent, nous sommes prêts à la personnalisation de texte.</span><span class="sxs-lookup"><span data-stu-id="2199b-266">Now, we're ready to text the customization.</span></span> <span data-ttu-id="2199b-267">Choisissez **Lancer l’application** à ouvrir l’application dans votre navigateur web, puis choisissez le bouton de barre d’Action FilterTasks personnalisé.</span><span class="sxs-lookup"><span data-stu-id="2199b-267">Choose **Launch App** to open the app in your web browser and then choose the custom FilterTasks Action Bar button.</span></span> <span data-ttu-id="2199b-268">Toutes les tâches après l’échéance ou arrivant à échéance dans les 7 prochains jours sont affichés.</span><span class="sxs-lookup"><span data-stu-id="2199b-268">Any tasks past due or due in the next 7 days are displayed.</span></span> <span data-ttu-id="2199b-269">Un message s’affiche si l’application ne contient aucune tâche urgents.</span><span class="sxs-lookup"><span data-stu-id="2199b-269">A message is displayed if the app contains no urgent tasks.</span></span> 
  
## <a name="conclusion"></a><span data-ttu-id="2199b-270">Conclusion</span><span class="sxs-lookup"><span data-stu-id="2199b-270">Conclusion</span></span>

<span data-ttu-id="2199b-271">Vous pouvez utiliser l’action de macro **RequeryRecords** dans une macro d’interface utilisateur pour filtrer l’affichage en fonction des critères que vous choisissez.</span><span class="sxs-lookup"><span data-stu-id="2199b-271">You can use the **RequeryRecords** macro action in a UI macro to filter the view based on the criteria that you choose.</span></span> <span data-ttu-id="2199b-272">Selon le comportement que vous le souhaitez, vous souhaiterez peut-être créer une macro de données pour vérifier qu’un enregistrement répond aux critères avant d’utiliser l’action de macro **RequeryRecords** .</span><span class="sxs-lookup"><span data-stu-id="2199b-272">Depending on the behavior that you want, you may want to create a data macro to verify that a record meets the criteria before you use the **RequeryRecords** macro action.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2199b-273">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2199b-273">See also</span></span>

- [<span data-ttu-id="2199b-274">Nouveautés d'Access pour les développeurs</span><span class="sxs-lookup"><span data-stu-id="2199b-274">What's new for Access 2013 developers</span></span>](http://msdn.microsoft.com/library/df778f51-d65e-4c30-b618-65003ceb39b3%28Office.15%29.aspx)
    

