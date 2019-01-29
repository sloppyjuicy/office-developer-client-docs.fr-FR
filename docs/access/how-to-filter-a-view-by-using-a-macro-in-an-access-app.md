---
title: Filtrage d’une vue à l’aide d’une macro dans l’application Access
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
ms.topic: overview
ms.assetid: db4dbb71-1b22-4dfd-bc07-5f7d694fc038
description: Découvrez comment filtrer un affichage dans une application Access à l’aide de l’action de macro RequeryRecords et une macro de données.
localization_priority: Priority
ms.openlocfilehash: 861851a3497f290fe0bcda38e51794194fbe7bbe
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726399"
---
# <a name="filter-a-view-by-using-a-macro-in-an-access-app"></a><span data-ttu-id="b2fe6-103">Filtrage d’une vue à l’aide d’une macro dans l’application Access</span><span class="sxs-lookup"><span data-stu-id="b2fe6-103">Filter a view by using a macro in an Access app</span></span>

<span data-ttu-id="b2fe6-104">Découvrez comment filtrer un affichage dans une application Access à l’aide de l’action de macro RequeryRecords et une macro de données.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-104">Learn how to filter a view in an Access app by using the RequeryRecords macro action and a data macro.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="b2fe6-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/fr-FR/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/fr-FR/) to build no-code business solutions for the web and mobile devices.</span></span> 

<span data-ttu-id="b2fe6-107">L’affichage de liste par défaut dans une application Access vous permet de filtrer les problèmes sur les valeurs contenues dans les champs.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-107">The default list view in an Access app enables you to filter the issues on values that are contained in the fields.</span></span> <span data-ttu-id="b2fe6-108">Vous voudrez peut-être filtrer un affichage en fonction d’un ensemble de conditions au lieu de la mise en correspondance d’une valeur.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-108">There may be instances where you'd like to filter a view based on a set of conditions instead of by matching a value.</span></span> <span data-ttu-id="b2fe6-109">Pour ce faire, vous devez créer une macro.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-109">To do that you must create a macro.</span></span> <span data-ttu-id="b2fe6-110">Cet article vous explique comment créer une macro qui filtre un affichage afin de présenter les tâches dont l’échéance est passée ou arrive dans les 7 prochains jours.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-110">This article shows you how to create a macro that filter a view to display tasks that are past due or due in the next 7 days.</span></span>
  
## <a name="prerequisites-for-building-an-app-with-access"></a><span data-ttu-id="b2fe6-111">Conditions préalables à la création d’une application avec Access</span><span class="sxs-lookup"><span data-stu-id="b2fe6-111">Prerequisites for building an app with Access 2013</span></span>
<span data-ttu-id="b2fe6-112"><a name="Access2013FilterViewByUsingMacro_Prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="b2fe6-112"></span></span>

<span data-ttu-id="b2fe6-113">Pour suivre les étapes de cet exemple, vous avez besoin des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="b2fe6-113">To follow the steps in this example, you need the following:</span></span>
  
- <span data-ttu-id="b2fe6-114">Access 2013</span><span class="sxs-lookup"><span data-stu-id="b2fe6-114">Access 2013</span></span>
- <span data-ttu-id="b2fe6-115">Un environnement de développement SharePoint 2013</span><span class="sxs-lookup"><span data-stu-id="b2fe6-115">A SharePoint 2013 development environment</span></span>
    
> [!NOTE]
> <span data-ttu-id="b2fe6-116">Pour plus d'informations sur la configuration de votre environnement de développement SharePoint, consultez [Configurer un environnement de développement général pour SharePoint 2013](https://msdn.microsoft.com/library/08e4e4e1-d960-43fa-85df-f3c279ed6927%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b2fe6-116">For more information about setting up your SharePoint development environment, see [Set up a general development environment for SharePoint 2013](https://msdn.microsoft.com/library/08e4e4e1-d960-43fa-85df-f3c279ed6927%28Office.15%29.aspx).</span></span> <span data-ttu-id="b2fe6-117">Pour plus d'informations sur l'obtention de Access 2013 et SharePoint 2013, consultez [Téléchargements](https://msdn.microsoft.com/office/apps/fp123627).</span><span class="sxs-lookup"><span data-stu-id="b2fe6-117">For more information about obtaining Access 2013 and SharePoint 2013, see [Downloads](https://msdn.microsoft.com/office/apps/fp123627).</span></span> 
  
## <a name="create-the-app"></a><span data-ttu-id="b2fe6-118">Création de l’application</span><span class="sxs-lookup"><span data-stu-id="b2fe6-118">Create the app</span></span>
<span data-ttu-id="b2fe6-119"><a name="Access2013FilterViewByUsingMacro_CreateApp"> </a></span><span class="sxs-lookup"><span data-stu-id="b2fe6-119"></span></span>

<span data-ttu-id="b2fe6-120">Supposons que vous vouliez créer une application Access qui assure le suivi des tâches pour votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-120">Suppose you want to create an Access app that tracks issues for your business.</span></span> <span data-ttu-id="b2fe6-121">Avant de commencer à créer les tables et affichages, vous devriez rechercher un modèle de schéma.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-121">Before you start creating the tables and view from scratch, you should search for a schema template that meets your needs.</span></span>
  
### <a name="to-create-the-task-tracking-app"></a><span data-ttu-id="b2fe6-122">Créer l’application de suivi des tâches</span><span class="sxs-lookup"><span data-stu-id="b2fe6-122">To create the issue tracking app</span></span>

1. <span data-ttu-id="b2fe6-123">Ouvrez Access, puis sélectionnez **Application web personnalisée**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-123">Open Access and choose **Custom web app**.</span></span>
    
2. <span data-ttu-id="b2fe6-p105">Entrez un nom et un emplacement web pour votre application. Vous pouvez également sélectionner un emplacement dans la liste **Emplacements**, puis sélectionner **Créer**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-p105">Enter a name and the web location for your app. You can also choose a location from the **Locations** list and choose **Create**.</span></span>
    
3. <span data-ttu-id="b2fe6-126">Saisissez les **tâches** dans la zone **Recherche**, puis appuyez sur ENTRÉE.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-126">Type **tasks** into the **Search** box and then press ENTER.</span></span> 
    
    <span data-ttu-id="b2fe6-127">La figure 1 présente la liste des modèles pouvant être utiles pour le suivi des tâches.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-127">A list of templates that might be useful for tracking issues is displayed in Figure 1.</span></span>
    
   <span data-ttu-id="b2fe6-128">**Figure 1. Modèles appropriés pour la recherche des tâches**</span><span class="sxs-lookup"><span data-stu-id="b2fe6-128">**Figure 1. Templates that match the search for issues**</span></span>

   <span data-ttu-id="b2fe6-129">![Modèles appropriés pour la recherche des problèmes](media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Modèles appropriés pour la recherche des problèmes")</span><span class="sxs-lookup"><span data-stu-id="b2fe6-129">![Templates that match the search for issues](media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Templates that match the search for issues")</span></span>
  
4. <span data-ttu-id="b2fe6-130">Sélectionnez **Tâches**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-130">Choose **Tasks**.</span></span>
    
<span data-ttu-id="b2fe6-131">Access crée un ensemble de tables et d’affichages.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-131">Access creates a set of tables and views.</span></span>
  
<span data-ttu-id="b2fe6-132">Saisissez plusieurs exemples de tâches et d’employés dans votre application.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-132">Enter several sample tasks and employees in your app.</span></span> <span data-ttu-id="b2fe6-133">À cette fin, cliquez sur **Lancer l’application** pour ouvrir l’application dans votre navigateur web.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-133">To do this, click **Launch App** to open the app in your web browser.</span></span> <span data-ttu-id="b2fe6-134">Saisissez une valeur dans le champ **Date d’échéance** pour chaque tâche.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-134">Enter a value in the **Due Date** field for each task.</span></span> <span data-ttu-id="b2fe6-135">Revenez à Access lorsque vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-135">Return to Access when you're done.</span></span> 
  
## <a name="plan-the-customizations"></a><span data-ttu-id="b2fe6-136">Planifier les personnalisations</span><span class="sxs-lookup"><span data-stu-id="b2fe6-136">Plan the customizations</span></span>
<span data-ttu-id="b2fe6-137"><a name="Access2013FilterViewByUsingMacro_PlanCustomizations"> </a></span><span class="sxs-lookup"><span data-stu-id="b2fe6-137"></span></span>

<span data-ttu-id="b2fe6-138">Vous avez désormais une application qui contient plusieurs tâches.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-138">You now have an app that contains several tasks.</span></span> <span data-ttu-id="b2fe6-139">L’affichage par défaut vous permet de rechercher les tâches utilisant des éléments stockés dans les champs présentés dans l’affichage.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-139">The default view enables you to search for any tasks using items that are stored in the fields displayed in the view.</span></span> <span data-ttu-id="b2fe6-140">Par exemple, vous pouvez rechercher les problèmes hautement prioritaires ou les problèmes en cours.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-140">For example, you can search for high-priority issues or issues in progress.</span></span> <span data-ttu-id="b2fe6-141">Supposons que vous vouliez hiérarchiser votre travail en affichant les problèmes actifs qui arrivent à échéance la semaine prochaine.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-141">Suppose you want to prioritize your work by displaying active issues that are due in the coming week.</span></span> <span data-ttu-id="b2fe6-142">Pour ce faire, vous devez créer une macro d’interface utilisateur (IU).</span><span class="sxs-lookup"><span data-stu-id="b2fe6-142">To do this, you should create a user interface (UI) macro.</span></span>
  
<span data-ttu-id="b2fe6-143">La commande de macro d’interface utilisateur que vous pouvez utiliser pour filtrer l’affichage est [RequeryRecords Macro Action (application web personnalisée Access)](requeryrecords-macro-action-access-custom-web-app.md).</span><span class="sxs-lookup"><span data-stu-id="b2fe6-143">The UI macro command that you can use to filter the view is the [RequeryRecords Macro Action (Access custom web app)](requeryrecords-macro-action-access-custom-web-app.md).</span></span> <span data-ttu-id="b2fe6-144">L’action de macro **RequeryRecords** permet de filtrer l’affichage basé sur l’argument *where*, fourni sous la forme d’une clause SQL WHERE.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-144">The **RequeryRecords** macro action filters the view based on the  *Where*  argument, which is provided in the form of a SQL WHERE clause.</span></span> <span data-ttu-id="b2fe6-145">Pour filtrer l’affichage, vous devez fournir plusieurs faits dans un format spécifique pour filtrer l’affichage.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-145">To filter the view, you must supply several facts in a specific format to filter the view.</span></span> 
  
<span data-ttu-id="b2fe6-146">Les faits pertinents sont :</span><span class="sxs-lookup"><span data-stu-id="b2fe6-146">The relevant facts are:</span></span>
  
- <span data-ttu-id="b2fe6-147">Le ou les champs à comparer</span><span class="sxs-lookup"><span data-stu-id="b2fe6-147">The field or fields to compare</span></span>
    
- <span data-ttu-id="b2fe6-148">Comment faire référence à la date du jour</span><span class="sxs-lookup"><span data-stu-id="b2fe6-148">How to refer to today's date</span></span>
    
- <span data-ttu-id="b2fe6-149">Comment faire référence à un jour spécifique par rapport à la date du jour</span><span class="sxs-lookup"><span data-stu-id="b2fe6-149">How to refer to a particular day relative to today's date</span></span>
    
- <span data-ttu-id="b2fe6-150">Comment identifier les tâches en cours</span><span class="sxs-lookup"><span data-stu-id="b2fe6-150">How to determine which on tasks are in progress</span></span>
    
<span data-ttu-id="b2fe6-151">Le champ **Date d’échéance** fournit des informations sur l’échéance d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-151">The **Due Date** field provides information about when a task is due.</span></span> <span data-ttu-id="b2fe6-152">Le champ **État** fournit des informations d’état des tâches.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-152">The **Status** field provides status information about each task.</span></span> <span data-ttu-id="b2fe6-153">Pour faire référence à un champ dans une macro, utilisez le format **[*TableName*].[*FieldName*]**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-153">To refer to a field in a macro, use the format **[*TableName*].[*FieldName*]**.</span></span> <span data-ttu-id="b2fe6-154">Utilisez **[Tasks].[Due Date]** pour faire référence au champ **Date d’échéance** et **[Tasks].[Status]** pour faire référence au champ **État**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-154">Use **[Tasks].[Due Date]** to refer to the **Due Date** field and **[Tasks].[Status]** to refer to the **Status** field.</span></span> 
  
<span data-ttu-id="b2fe6-155">La fonction [Fonction Today (application web personnalisée Access)](today-function-access-custom-web-app.md) renvoie la date du jour.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-155">The [Today Function (Access custom web app)](today-function-access-custom-web-app.md) function returns today's date.</span></span> <span data-ttu-id="b2fe6-156">La fonction [Fonction DateAdd (application web personnalisée Access)](dateadd-function-access-custom-web-app.md) peut être utilisée pour calculer une date qui correspond à un certain nombre de jours après une date spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-156">The [DateAdd Function (Access custom web app)](dateadd-function-access-custom-web-app.md) function can be used to calculate a date that's a certain number of days after a specified date.</span></span> 
  
<span data-ttu-id="b2fe6-157">Le champ **État** contient plusieurs valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-157">The **Status** field contains several possible values.</span></span> <span data-ttu-id="b2fe6-158">Une valeur **Terminée** indique que la tâche n’est plus active.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-158">A value of **Completed** indicates that the task is no longer active.</span></span> 
  
<span data-ttu-id="b2fe6-159">Ces faits peuvent être regroupés dans la clause suivante SQL WHERE.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-159">These facts can be combined into the following SQL WHERE clause.</span></span>
  
```sql
[Tasks].[Due Date]<DateAdd(Day,7,Today()) AND [Tasks].[Status]<>"Completed"
```

<span data-ttu-id="b2fe6-160">Cette clause SQL WHERE est utilisée dans la macro pour filtrer l’affichage afin de présenter les problèmes actifs dont l’échéance est passée ou arrive dans les 7 prochains jours.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-160">This SQL WHERE clause is used in the macro to filter the view to display active issues that are due in the next 7 days or are past due.</span></span>
  
<span data-ttu-id="b2fe6-161">Pour exécuter la macro d’interface utilisateur, elle doit être liée à un élément ou à un événement qui survient dans l’affichage.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-161">To run the UI macro, it must be attached to an item or an event that occurs in the view.</span></span> <span data-ttu-id="b2fe6-162">La **barre d’action** est un endroit pratique pour ajouter une commande personnalisée à l’affichage.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-162">The **Action Bar** is a convenient place to add a custom command to the view.</span></span> <span data-ttu-id="b2fe6-163">La **barre d’action** est une barre d’outils personnalisable qui s’affiche en haut de chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-163">The Action Bar is a customizable toolbar that appears at the top of each view, as shown in Figure 5.</span></span> <span data-ttu-id="b2fe6-164">Par défaut, la **barre d’action** contient des boutons pour ajouter, modifier, enregistrer, supprimer et annuler des modifications.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-164">By default, the **Action Bar** contains buttons to add, edit, save, delete, and cancel edits.</span></span> <span data-ttu-id="b2fe6-165">Vous pouvez ajouter des boutons qui effectuent des actions personnalisées, telles que le filtrage de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-165">You can add buttons that perform custom actions, such as filtering the view.</span></span> 
  
<span data-ttu-id="b2fe6-166">Si l’affichage contient des enregistrements répondant aux critères spécifiés, **RequeryRecords** filtre alors l’affichage.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-166">If the view contains records that meet the specified criteria, then **RequeryRecords** filters the view.</span></span> <span data-ttu-id="b2fe6-167">Cependant, si l’affichage ne contient pas d’enregistrements qui répondent aux critères, un nouvel enregistrement vide s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-167">However, if the view doesn't contain any records that meet the criteria, than a new, blank record is displayed.</span></span> <span data-ttu-id="b2fe6-168">Si vous ne souhaitez pas afficher un enregistrement vide si aucune des tâches n’arrive à échéance la semaine suivante, vous devez trouver une méthode pour vérifier les tâches avant d’appeler l’action de macro **RequeryRecords**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-168">If you don't want a blank record to be displayed if no tasks are due in the next week, then you must find a method to check the tasks before you call the **RequeryRecords** macro action.</span></span> <span data-ttu-id="b2fe6-169">Pour ce faire, créez une macro de données pour rechercher les enregistrements qui répondent aux critères.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-169">To do this, create a data macro to check for records that meet the criteria.</span></span> 
  
<span data-ttu-id="b2fe6-170">La macro d’interface utilisateur va appeler la macro de données, qui va tenter de trouver une tâche dont l’échéance arrive la semaine suivante.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-170">The UI macro will call the data macro, which will try to find a task that's due in the next week.</span></span> <span data-ttu-id="b2fe6-171">Si la macro de données trouve la tâche, personnalisez ensuite l’application.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-171">If the data macro finds the task then customize the app.</span></span>
  
## <a name="customize-the-app"></a><span data-ttu-id="b2fe6-172">Personnalisation de l’application</span><span class="sxs-lookup"><span data-stu-id="b2fe6-172">Customize the app</span></span>
<span data-ttu-id="b2fe6-173"><a name="Access2013FilterViewByUsingMacro_CustomizeApp"> </a></span><span class="sxs-lookup"><span data-stu-id="b2fe6-173"></span></span>

<span data-ttu-id="b2fe6-174">À présent que vous avez déterminé les personnalisations, implémentez-les.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-174">Now that you've determined the customizations, implement them.</span></span> <span data-ttu-id="b2fe6-175">Vous devriez créer la macro de données en premier.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-175">The data macro should be created first.</span></span> <span data-ttu-id="b2fe6-176">Certaines macros de données sont liées directement aux tables.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-176">Some data macros are attached directly to tables.</span></span> <span data-ttu-id="b2fe6-177">Cependant, cette macro de données est une macro de données autonome.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-177">However, this data macro is a stand-alone data macro.</span></span>
  
### <a name="to-create-the-data-macro"></a><span data-ttu-id="b2fe6-178">Créer la macro de données</span><span class="sxs-lookup"><span data-stu-id="b2fe6-178">To create the AfterUpdate macro</span></span>

1. <span data-ttu-id="b2fe6-179">Ouvrez l’application dans Access.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-179">Open the app in Access.</span></span>
    
2. <span data-ttu-id="b2fe6-180">Dans le groupe **Créer**, sélectionnez **Avancé**, puis **Macro de données**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-180">In the **Create** group, choose **Advanced**, and then choose **Data Macro**.</span></span>
    
    <span data-ttu-id="b2fe6-181">Une macro de données vide s’ouvre dans l’affichage Création de macros.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-181">A blank macro is opened in macro Design View.</span></span>
    
3. <span data-ttu-id="b2fe6-182">Dans la zone de liste **Ajouter une nouvelle action**, sélectionnez **LookupRecord**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-182">From the **Add New Action** dropdown, choose **LookupRecord**.</span></span>
    
4. <span data-ttu-id="b2fe6-183">Dans la zone de liste **Rechercher un enregistrement**, sélectionnez **Tâches**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-183">In the **Look Up A Record In** dropdown, choose **Customers**.</span></span>
    
5. <span data-ttu-id="b2fe6-184">Dans la zone **Condition Where**, saisissez **[Tasks].[Due Date]\<DateAdd(Day,7,Today()) AND [Tasks].[Status]\<\>"Completed"**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-184">In the **Where Condition** box, enter **[Tasks].[Due Date]\<DateAdd(Day,7,Today()) AND [Tasks].[Status]\<\>"Completed"**.</span></span> 
    
6. <span data-ttu-id="b2fe6-185">Dans la zone de liste **Ajouter une nouvelle Action**, sélectionnez **SetReturnVar**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-185">Choose **SetReturnVar** from the **Add New Action** dropdown.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="b2fe6-186">Vous verrez deux zones de liste **Ajouter une nouvelle action** : une au sein du bloc **LookupRecord** et une autre extérieure au bloc **LookupRecord**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-186">You'll see two **Add New Action** dropdowns, one within the **LookupRecord** block, and another outside the **LookupRecord** block.</span></span> <span data-ttu-id="b2fe6-187">Vous devez sélectionner la zone de liste **Ajouter une nouvelle action** dans le bloc **LookupRecord**, comme illustré dans la Figure 1.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-187">You should choose the **Add New Action** dropdown within the **LookupRecord** block, as shown in Figure 7.</span></span> 
  
   <span data-ttu-id="b2fe6-188">**Figure 1. Zone de liste Ajouter une nouvelle action**</span><span class="sxs-lookup"><span data-stu-id="b2fe6-188">**Figure 1. Add New Action list box**</span></span>

   <span data-ttu-id="b2fe6-189">![Liste déroulante Ajouter une nouvelle Action](media/odc_Access2013_FilterFormByUsingMacro_Figure01.jpg "Liste déroulante Ajouter une nouvelle action")</span><span class="sxs-lookup"><span data-stu-id="b2fe6-189">![Add New Action dropdown](media/odc_Access2013_FilterFormByUsingMacro_Figure01.jpg "Add New Action dropdown")</span></span>
  
7. <span data-ttu-id="b2fe6-190">Dans la zone **Nom**, saisissez **TaskFound**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-190">In the **Name** box, enter **ContactPhone**.</span></span> 
    
8. <span data-ttu-id="b2fe6-191">Dans la zone **Expression**, saisissez **« Yes »**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-191">In the **Expression** box, enter **[Customers].[Work Phone]**.</span></span> 
    
9. <span data-ttu-id="b2fe6-192">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-192">Choose **Save**.</span></span> <span data-ttu-id="b2fe6-193">Dans la zone **Nom de macro**, saisissez **TasksDueSoon**, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-193">Enter **GetContactPhone** in the **Macro Name** box and then choose **OK**.</span></span>
    
    <span data-ttu-id="b2fe6-194">La macro doit ressembler à celle illustrée à la figure 2.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-194">The macro should resemble the macro shown in Figure 9.</span></span>
    
   <span data-ttu-id="b2fe6-195">**Figure 2. Macro de données TasksDueSoon**</span><span class="sxs-lookup"><span data-stu-id="b2fe6-195">**Figure 2. TasksDueSoon data macro**</span></span>

   <span data-ttu-id="b2fe6-196">![Macro de données TasksDueSoon](media/odc_Access2013_FilterFormByUsingMacro_Figure02.jpg "Macro de données TasksDueSoon")</span><span class="sxs-lookup"><span data-stu-id="b2fe6-196">![TasksDueSoon data macro](media/odc_Access2013_FilterFormByUsingMacro_Figure02.jpg "TasksDueSoon data macro")</span></span>
  
10. <span data-ttu-id="b2fe6-197">Fermez l’affichage Création de macros.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-197">Close macro Design View.</span></span>
    
<span data-ttu-id="b2fe6-198">À présent, nous sommes prêts à ajouter un bouton personnalisé à la barre d’action.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-198">Now, we're ready to add a custom button to the Action Bar.</span></span>
  
### <a name="to-add-a-custom-button-to-the-action-bar"></a><span data-ttu-id="b2fe6-199">Ajouter un bouton personnalisé à la barre d’action</span><span class="sxs-lookup"><span data-stu-id="b2fe6-199">To add a custom button to the Action Bar</span></span>

1. <span data-ttu-id="b2fe6-200">Sélectionnez la table **Tâches**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-200">Choose the **Issues** table.</span></span> <span data-ttu-id="b2fe6-201">Cette action choisit le formulaire Liste de tâches.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-201">This chooses the Tasks List form.</span></span> 
    
2. <span data-ttu-id="b2fe6-202">Dans le sélecteur d’affichage, sélectionnez **Liste**, l’icône **Paramètres/Action**, puis **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-202">In the View selector, choose **List**, choose the **Settings/Action** icon, and then choose **Edit**.</span></span>
    
    <span data-ttu-id="b2fe6-203">L’affichage est ouvert en mode Création.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-203">The view is opened in Design View.</span></span>
    
3. <span data-ttu-id="b2fe6-204">À présent, nous sommes prêts à ajouter un bouton personnalisé à la barre d’action.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-204">Now, we're ready to add a custom button to the Action Bar.</span></span> <span data-ttu-id="b2fe6-205">Pour ce faire, sélectionnez **Ajouter une action personnalisée** comme illustré dans la Figure 3.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-205">To do this, choose **Add custom action** as shown in Figure 3.</span></span> 
    
   <span data-ttu-id="b2fe6-206">**Figure 3. Bouton Ajouter une action personnalisée**</span><span class="sxs-lookup"><span data-stu-id="b2fe6-206">**Figure 3. Add custom action button**</span></span>

   <span data-ttu-id="b2fe6-207">![Bouton Ajouter une action personnalisée](media/odc_Access2013_FilterFormByUsingMacro_Figure03.jpg "Bouton Ajouter une action personnalisée")</span><span class="sxs-lookup"><span data-stu-id="b2fe6-207">![Add custom action button](media/odc_Access2013_FilterFormByUsingMacro_Figure03.jpg "Add custom action button")</span></span>
  
    <span data-ttu-id="b2fe6-208">La nouvelle action est représentée par un bouton en forme étoile comme illustré dans la Figure 4.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-208">The new action is displayed as a button with a star icon as shown in Figure 4.</span></span>
    
   <span data-ttu-id="b2fe6-209">**Figure 4. Nouveau bouton de la barre d’action**</span><span class="sxs-lookup"><span data-stu-id="b2fe6-209">**Figure 4. New Action Bar button**</span></span>

   <span data-ttu-id="b2fe6-210">![Nouveau bouton de la barre d’action](media/odc_Access2013_FilterFormByUsingMacro_Figure04.jpg "Nouveau bouton de la barre d’action")</span><span class="sxs-lookup"><span data-stu-id="b2fe6-210">![New Action Bar button](media/odc_Access2013_FilterFormByUsingMacro_Figure04.jpg "New Action Bar button")</span></span>
  
4. <span data-ttu-id="b2fe6-211">Sélectionnez le bouton de barre d’action personnalisé, puis sélectionnez l’icône **Données**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-211">Choose the custom Action Bar Button, and then choose the **Data** icon.</span></span> 
    
    <span data-ttu-id="b2fe6-212">La boîte de dialogue **Données** apparaît.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-212">The **Export** dialog box appears.</span></span> 
    
5. <span data-ttu-id="b2fe6-213">Dans la zone **Nom du contrôle**, saisissez **FilterTasks**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-213">In the **Control Name** box, enter **CustomerContact**.</span></span> 
    
6. <span data-ttu-id="b2fe6-214">Dans la zone **Info-bulle**, saisissez **Afficher les tâches dont l’échéance est passée ou arrive la semaine suivante**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-214">In the **Tooltip** box, enter **Display tasks past due or due in the next week**.</span></span> 
    
<span data-ttu-id="b2fe6-215">À présent, nous sommes prêts à créer la macro d’interface utilisateur qui va filtrer l’affichage.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-215">Now, we're ready to create the UI macro that will filter the view.</span></span>
  
### <a name="to-create-the-ui-macro-to-filter-the-view"></a><span data-ttu-id="b2fe6-216">Créer la macro d’interface utilisateur pour filtrer l’affichage</span><span class="sxs-lookup"><span data-stu-id="b2fe6-216">To create the UI macro to filter the view</span></span>

1. <span data-ttu-id="b2fe6-217">Dans la boîte de dialogue **Données**, choisissez **Sur clic** comme illustré dans la Figure 5.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-217">In the **Data** dialog box, choose **On Click** as shown in Figure 5.</span></span> 
    
   <span data-ttu-id="b2fe6-218">**Figure 5. Boîte de dialogue Données**</span><span class="sxs-lookup"><span data-stu-id="b2fe6-218">**Figure 5. Local intranet dialog box**</span></span>

   <span data-ttu-id="b2fe6-219">![Boîte de dialogue Données](media/odc_Access2013_FilterFormByUsingMacro_Figure05.jpg "Boîte de dialogue Données")</span><span class="sxs-lookup"><span data-stu-id="b2fe6-219">![Data dialog box](media/odc_Access2013_FilterFormByUsingMacro_Figure05.jpg "Data dialog box")</span></span>
  
    <span data-ttu-id="b2fe6-220">Une macro d’interface utilisateur vide s’ouvre dans l’affichage Création de macros.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-220">A blank macro is opened in macro Design View.</span></span>
    
2. <span data-ttu-id="b2fe6-221">Dans la zone de liste **Ajouter une nouvelle action**, sélectionnez **RunDataMacro**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-221">From the **Add New Action** dropdown, choose **RunDataMacro**.</span></span> 
    
3. <span data-ttu-id="b2fe6-222">Dans la zone Nom de Macro, saisissez **TasksDueSoon**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-222">In the Name box, enter ContactPhone.</span></span> 
    
    <span data-ttu-id="b2fe6-223">Dans la zone **SetLocalVar**, saisissez **FilterRecords**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-223">In the **SetLocalVar** box, enter **Phone**.</span></span> 
    
    <span data-ttu-id="b2fe6-224">L’action **RunDataMacro** appelle la macro de données **TasksDueSoon** que nous avons créée précédemment et enregistre son résultat dans une variable nommée **FilterRecords**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-224">The **RunDataMacro** action calls the **TasksDueSoon** data macro we created earlier and stores its result in a variable named **FilterRecords**.</span></span> 
    
4. <span data-ttu-id="b2fe6-225">Dans la zone de liste **Ajouter une nouvelle action**, sélectionnez **If**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-225">From the **Add New Action** list box, choose **If**.</span></span> 
    
5. <span data-ttu-id="b2fe6-226">Dans la zone **If**, saisissez **[FilterRecords]="Yes"**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-226">In the **If** box, enter **[FilterRecords]="Yes"**.</span></span> 
    
6. <span data-ttu-id="b2fe6-227">Dans la zone de liste **Ajouter une nouvelle action**, sélectionnez **RequeryRecords**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-227">From the **Add New Action** list box, choose **RequeryRecords**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="b2fe6-228">Vous verrez deux zones de liste **Ajouter une nouvelle action** : une au sein du bloc **If** et une autre extérieure au bloc **If**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-228">You'll see two **Add New Action** dropdowns, one within the **LookupRecord** block, and another outside the **LookupRecord** block.</span></span> <span data-ttu-id="b2fe6-229">Vous devez sélectionner la zone de liste **Ajouter une nouvelle action** dans le bloc **If**, comme illustré dans la Figure 6.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-229">You should choose the **Add New Action** dropdown within the **LookupRecord** block, as shown in Figure 7.</span></span> 
  
   <span data-ttu-id="b2fe6-230">**Figure 6. Zone de liste Ajouter une nouvelle action**</span><span class="sxs-lookup"><span data-stu-id="b2fe6-230">**Figure 6. Add New Action list box**</span></span>

   <span data-ttu-id="b2fe6-231">![Liste déroulante Ajouter une nouvelle Action](media/odc_Access2013_FilterFormByUsingMacro_Figure06.jpg "Liste déroulante Ajouter une nouvelle action")</span><span class="sxs-lookup"><span data-stu-id="b2fe6-231">![Add New Action dropdown](media/odc_Access2013_FilterFormByUsingMacro_Figure06.jpg "Add New Action dropdown")</span></span>
  
7. <span data-ttu-id="b2fe6-232">Dans la zone **Where**, saisissez \*\* [Tasks].[Due Date]\<DateAdd(Day,7,Today()) AND [Tasks].[Status]\<\>"Completed"\*\*.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-232">In the **Where** box, enter **[Tasks].[Due Date]\<DateAdd(Day,7,Today()) AND [Tasks].[Status]\<\>"Completed"**.</span></span> 
    
8. <span data-ttu-id="b2fe6-233">Dans la zone **Trier par**, saisissez **[Date d’échéance]**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-233">In the **Order By** box, enter **[Due Date]**.</span></span> 
    
9. <span data-ttu-id="b2fe6-234">Sélectionnez le lien **Ajouter Sinon** qui apparaît en regard de la zone **Ajouter une nouvelle action** comme illustré dans la Figure 7.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-234">Choose the **Add Else** link that appears to the right side of the **Add New Action** box as shown in Figure 7.</span></span> 
    
   <span data-ttu-id="b2fe6-235">**Figure 7. Lien Ajouter sinon**</span><span class="sxs-lookup"><span data-stu-id="b2fe6-235">**Figure 7. Add Patients link**</span></span>

   <span data-ttu-id="b2fe6-236">![Lien Ajouter sinon](media/odc_Access2013_FilterFormByUsingMacro_Figure07.jpg "Lien Ajouter sinon")</span><span class="sxs-lookup"><span data-stu-id="b2fe6-236">![Add Else link](media/odc_Access2013_FilterFormByUsingMacro_Figure07.jpg "Add Else link")</span></span>
  
    <span data-ttu-id="b2fe6-237">Une clause Else est ajoutée au bloc If.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-237">An Else clause is added to the If block.</span></span>
    
10. <span data-ttu-id="b2fe6-238">Dans la zone de liste **Ajouter une nouvelle action**, sélectionnez **MessageBox**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-238">From the **Add New Action** list box, choose **MessageBox**.</span></span> 
    
11. <span data-ttu-id="b2fe6-239">Dans la zone **Message**, saisissez **Aucune tâche dont l’échéance est passée ou qui arrive dans les 7 prochains jours !**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-239">In the **Message** box, enter **No tasks are overdue or due in the next 7 days!**.</span></span> 
    
12. <span data-ttu-id="b2fe6-240">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-240">Choose **Save**.</span></span>
    
    <span data-ttu-id="b2fe6-241">La macro doit ressembler celle illustrée à la figure 8.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-241">The macro should resemble the macro shown in Figure 8.</span></span>
    
    <span data-ttu-id="b2fe6-242">**Figure 8. Macro d’interface utilisateur pour filtrer l’affichage**</span><span class="sxs-lookup"><span data-stu-id="b2fe6-242">**UI macro to filter the view**</span></span>

    <span data-ttu-id="b2fe6-243">![Macro d’interface utilisateur pour filtrer l’affichage](media/odc_Access2013_FilterFormByUsingMacro_Figure08.jpg "Macro d’interface utilisateur pour filtrer l’affichage")</span><span class="sxs-lookup"><span data-stu-id="b2fe6-243">![UI macro to filter the view](media/odc_Access2013_FilterFormByUsingMacro_Figure08.jpg "UI macro to filter the view")</span></span>
  
13. <span data-ttu-id="b2fe6-244">Fermez l’affichage Création de macros.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-244">Close macro Design View.</span></span>
    
<span data-ttu-id="b2fe6-245">À ce stade, nous avons créé la macro d’interface utilisateur qui permet de filtrer l’affichage Liste des tâches afin de présenter les tâches urgentes.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-245">At this point, we've created the UI macro that filters the Tasks List view to display the urgent tasks.</span></span> <span data-ttu-id="b2fe6-246">Il serait déplacé de laisser l’affichage dans un état filtré sans fournir de méthode pour supprimer le filtre.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-246">It wouldn't be polite to leave the view in a filtered state without providing a method to remove the filter.</span></span> <span data-ttu-id="b2fe6-247">Pour ce faire, ajoutez un autre bouton de barre d’action et une macro d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-247">To do this, add another Action Bar button and UI Macro.</span></span>
  
### <a name="to-add-an-action-bar-button-to-remove-the-filter"></a><span data-ttu-id="b2fe6-248">Ajouter un bouton de barre d’action pour supprimer le filtre</span><span class="sxs-lookup"><span data-stu-id="b2fe6-248">To add an Action Bar Button to remove the filter</span></span>

1. <span data-ttu-id="b2fe6-249">Sélectionnez **Ajouter une action personnalisée**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-249">Choose **Add custom action**.</span></span>
    
    <span data-ttu-id="b2fe6-250">La nouvelle action est représentée par un bouton en forme étoile.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-250">The new action is displayed as a button with a star icon</span></span>
    
2. <span data-ttu-id="b2fe6-251">Sélectionnez le bouton de barre d’action personnalisé, puis l’icône **Données**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-251">Choose the custom Action Bar button, and then choose the **Data** icon.</span></span> 
    
    <span data-ttu-id="b2fe6-252">La boîte de dialogue **Données** apparaît.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-252">The **Export** dialog box appears.</span></span> 
    
3. <span data-ttu-id="b2fe6-253">Dans la zone **Nom du contrôle**, saisissez **RemoveFilter**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-253">In the **Control Name** box, enter **CustomerContact**.</span></span> 
    
4. <span data-ttu-id="b2fe6-254">Dans la zone **Info-bulle**, saisissez **Supprimer tous les filtres appliqués à l’affichage**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-254">In the **Tooltip** box, enter **Remove all filter applied to the view**.</span></span> 
    
<span data-ttu-id="b2fe6-255">À présent, nous sommes prêts à créer la macro d’interface utilisateur qui va supprimer le filtre de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-255">Now, we're ready to create the UI macro that will remove the filter form the view.</span></span>
  
### <a name="to-create-the-ui-macro-to-remove-the-filter-from-the-view"></a><span data-ttu-id="b2fe6-256">Créer la macro d’interface utilisateur pour supprimer le filtre de l’affichage</span><span class="sxs-lookup"><span data-stu-id="b2fe6-256">To create the UI macro to remove the filter from the view</span></span>

1. <span data-ttu-id="b2fe6-257">Dans la boîte de dialogue **Données**, choisissez **Sur clic**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-257">In the **Data** dialog box, choose **On Click**.</span></span>
    
    <span data-ttu-id="b2fe6-258">Une macro d’interface utilisateur vide s’ouvre dans l’affichage Création de macros.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-258">A blank macro is opened in macro Design View.</span></span>
    
2. <span data-ttu-id="b2fe6-259">Dans la zone de liste **Ajouter une nouvelle action**, sélectionnez **RequeryRecords**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-259">From the **Add New Action** list box, choose **RequeryRecords**.</span></span> 
    
    <span data-ttu-id="b2fe6-260">Cette fois, laissez les zones **Where** et **Trier par** vides.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-260">This time, we'll leave the **Where** and **Order By** boxes empty.</span></span> <span data-ttu-id="b2fe6-261">L’action **RequeryRecords** est ainsi appelée sans paramètres ; tous les filtres sont supprimés de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-261">Then the **RequeryRecords** action is called without any parameters, all filters are removed from the view.</span></span> 
    
3. <span data-ttu-id="b2fe6-262">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-262">Choose **Save**.</span></span>
    
4. <span data-ttu-id="b2fe6-263">Fermez l’affichage Création de macros.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-263">Close macro Design View.</span></span>
    
5. <span data-ttu-id="b2fe6-264">Fermez l’affichage Liste des problèmes.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-264">Close the Issues List view.</span></span> <span data-ttu-id="b2fe6-265">Lorsque vous êtes invité à enregistrer vos modifications, sélectionnez **Oui**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-265">Choose **Yes** when you are prompted to save your changes.</span></span> 
    
<span data-ttu-id="b2fe6-266">À présent, nous sommes prêts pour la personnalisation du texte.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-266">Now we're ready to text the customization.</span></span> <span data-ttu-id="b2fe6-267">Sélectionnez **Lancer l’application** pour ouvrir l’application dans votre navigateur web, puis le bouton de barre d’action personnalisé FilterTasks.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-267">Choose **Launch App** to open the app in your web browser and then choose the custom FilterTasks Action Bar button.</span></span> <span data-ttu-id="b2fe6-268">Les tâches dont l’échéance est passée ou arrive dans les 7 prochains jours sont affichées.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-268">Any tasks past due or due in the next 7 days are displayed.</span></span> <span data-ttu-id="b2fe6-269">Un message s’affiche si l’application ne contient aucune tâche urgente.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-269">A message is displayed if the app contains no urgent tasks.</span></span> 
  
## <a name="conclusion"></a><span data-ttu-id="b2fe6-270">Conclusion</span><span class="sxs-lookup"><span data-stu-id="b2fe6-270">Conclusion</span></span>

<span data-ttu-id="b2fe6-271">Vous pouvez utiliser l’action de macro **RequeryRecords** dans une macro d’interface utilisateur pour filtrer l’affichage en fonction des critères de votre choix.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-271">You can use the **RequeryRecords** macro action in a UI macro to filter the view based on the criteria that you choose.</span></span> <span data-ttu-id="b2fe6-272">En fonction du comportement recherché, vous pouvez être amené à créer une macro de données pour vérifier qu’un enregistrement répond aux critères avant d’utiliser l’action de macro **RequeryRecords**.</span><span class="sxs-lookup"><span data-stu-id="b2fe6-272">Depending on the behavior that you want, you may want to create a data macro to verify that a record meets the criteria before you use the **RequeryRecords** macro action.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b2fe6-273">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2fe6-273">See also</span></span>

- [<span data-ttu-id="b2fe6-274">Nouveautés d’Access 2013 pour les développeurs</span><span class="sxs-lookup"><span data-stu-id="b2fe6-274">What's new for Access 2013 developers</span></span>](https://msdn.microsoft.com/library/df778f51-d65e-4c30-b618-65003ceb39b3%28Office.15%29.aspx)
    

