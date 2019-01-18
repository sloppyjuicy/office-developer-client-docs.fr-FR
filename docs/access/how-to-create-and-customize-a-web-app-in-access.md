---
title: Création et personnalisation d’une application web dans Access
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: 628745f4-82e9-4838-9726-6f3e506a654f
localization_priority: Priority
ms.openlocfilehash: d7d27e98189a5b6784e4db48c81a545b85f01fc1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716816"
---
# <a name="create-and-customize-a-web-app-in-access"></a><span data-ttu-id="671cb-102">Création et personnalisation d’une application web dans Access</span><span class="sxs-lookup"><span data-stu-id="671cb-102">Create and customize a web app in Access</span></span>

> [!IMPORTANT]
> <span data-ttu-id="671cb-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="671cb-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
<span data-ttu-id="671cb-p102">Access 2013 propose un nouveau modèle d'application qui permet aux experts de créer rapidement des applications pour le web. Access inclut un ensemble de modèles qui vous permettent de commencer à créer votre application.</span><span class="sxs-lookup"><span data-stu-id="671cb-p102">Access 2013 features a new application model that enables subject matter experts to quickly create web-based applications. Included with Access are a set of templates that you can use to jump start creating your application.</span></span>

<span data-ttu-id="671cb-107"><a name="ac15_CreateAndCustomizeWebApp_Prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="671cb-107"><a name="ac15_CreateAndCustomizeWebApp_Prerequisites"> </a></span></span>

## <a name="prerequisites-for-building-an-app-with-access-2013"></a><span data-ttu-id="671cb-108">Conditions préalables à la création d'une application avec Access 2013</span><span class="sxs-lookup"><span data-stu-id="671cb-108">Prerequisites for building an app with Access 2013</span></span>

<span data-ttu-id="671cb-109">Pour suivre les étapes de cet exemple, vous avez besoin des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="671cb-109">To follow the steps in this example, you need the following:</span></span>
  
- <span data-ttu-id="671cb-110">Access</span><span class="sxs-lookup"><span data-stu-id="671cb-110">Access</span></span>
    
- <span data-ttu-id="671cb-111">Un environnement de développement SharePoint</span><span class="sxs-lookup"><span data-stu-id="671cb-111">A SharePoint development environment</span></span>
    
<span data-ttu-id="671cb-112">Pour plus d'informations sur la configuration de votre environnement de développement SharePoint, consultez [Configurer un environnement de développement général pour SharePoint](https://docs.microsoft.com/sharepoint/dev/general-development/set-up-a-general-development-environment-for-sharepoint).</span><span class="sxs-lookup"><span data-stu-id="671cb-112">For more information about setting up your SharePoint development environment, see [Set up a general development environment for SharePoint](https://docs.microsoft.com/sharepoint/dev/general-development/set-up-a-general-development-environment-for-sharepoint).</span></span> 
  
<span data-ttu-id="671cb-113">Pour plus d'informations sur l'obtention d’Access et SharePoint, consultez [Téléchargements](https://msdn.microsoft.com/office/apps/fp123627).</span><span class="sxs-lookup"><span data-stu-id="671cb-113">For more information about obtaining Access and SharePoint, see [Downloads](https://msdn.microsoft.com/office/apps/fp123627).</span></span>

<span data-ttu-id="671cb-114"><a name="ac15_CreateAndCustomizeWebApp_CreateTheApp"> </a></span><span class="sxs-lookup"><span data-stu-id="671cb-114"><a name="ac15_CreateAndCustomizeWebApp_CreateTheApp"> </a></span></span>

## <a name="create-the-app"></a><span data-ttu-id="671cb-115">Création de l'application</span><span class="sxs-lookup"><span data-stu-id="671cb-115">Create the app</span></span>

<span data-ttu-id="671cb-p103">Supposons que vous vouliez créer une application Access qui assure le suivi des problèmes pour votre entreprise. Avant de commencer à créer les tables et affichages à partir de rien, vous devriez rechercher un modèle de schéma correspondant à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="671cb-p103">Suppose you want to create an Access app that tracks issues for your business. Before you start creating the tables and view from scratch, you should search for a schema template that meets your needs.</span></span>
  
### <a name="to-create-the-issue-tracking-app"></a><span data-ttu-id="671cb-118">Pour créer l'application de suivi des problèmes</span><span class="sxs-lookup"><span data-stu-id="671cb-118">To create the issue tracking app</span></span>

1. <span data-ttu-id="671cb-119">Ouvrez Access, puis sélectionnez **Application web personnalisée**.</span><span class="sxs-lookup"><span data-stu-id="671cb-119">Open Access and choose **Custom web app**.</span></span>
    
2. <span data-ttu-id="671cb-p104">Entrez un nom et un emplacement web pour votre application. Vous pouvez également sélectionner un emplacement dans la liste **Emplacements**, puis sélectionner **Créer**.</span><span class="sxs-lookup"><span data-stu-id="671cb-p104">Enter a name and the web location for your app. You can also choose a location from the **Locations** list and choose **Create**.</span></span>
    
3. <span data-ttu-id="671cb-122">Dans le champ **Quels sont les éléments dont vous souhaitez effectuer le suivi ?**, entrez **Problèmes**, puis appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="671cb-122">Type **Issues** into the **What would you like to track?** box and then press ENTER.</span></span> 
    
   <span data-ttu-id="671cb-123">La figure 1 présente la liste des modèles pouvant être utiles pour le suivi des problèmes.</span><span class="sxs-lookup"><span data-stu-id="671cb-123">A list of templates that might be useful for tracking issues is displayed in Figure 1.</span></span>
    
   <span data-ttu-id="671cb-124">**Figure 1. Modèles appropriés pour la recherche des problèmes**</span><span class="sxs-lookup"><span data-stu-id="671cb-124">**Figure 1. Templates that match the search for issues**</span></span>

   <span data-ttu-id="671cb-125">![Modèles appropriés pour la recherche des problèmes](media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Modèles appropriés pour la recherche des problèmes")</span><span class="sxs-lookup"><span data-stu-id="671cb-125">![Templates that match the search for issues](media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Templates that match the search for issues")</span></span>
  
4. <span data-ttu-id="671cb-126">Sélectionnez **Problèmes**.</span><span class="sxs-lookup"><span data-stu-id="671cb-126">Choose **Issues**.</span></span>
    
<span data-ttu-id="671cb-127">Access crée un ensemble de tables et d'affichages.</span><span class="sxs-lookup"><span data-stu-id="671cb-127">Access creates a set of tables and views.</span></span>
  
## <a name="explore-the-app"></a><span data-ttu-id="671cb-128">Exploration de l'application</span><span class="sxs-lookup"><span data-stu-id="671cb-128">Explore the app</span></span>
<span data-ttu-id="671cb-129"><a name="ac15_CreateAndCustomizeWebApp_ExploreTheApp"> </a></span><span class="sxs-lookup"><span data-stu-id="671cb-129"><a name="ac15_CreateAndCustomizeWebApp_ExploreTheApp"> </a></span></span>

<span data-ttu-id="671cb-130">Pour savoir si le schéma et les affichages répondent à vos besoins, vous devez les examiner.</span><span class="sxs-lookup"><span data-stu-id="671cb-130">To understand whether the schema and views meet your needs, you should examine them.</span></span>
  
<span data-ttu-id="671cb-p105">Les tables créées en sélectionnant le schéma Problèmes s'affichent dans le volet en mosaïque. Les tables Problèmes, Clients et Employés constituent la cible principale de l'application. La table Problèmes stocke des informations sur chaque problème. Chaque problème est attribué à l'employé qui l'ouvre au nom d'un client. Les tables Problèmes connexes et Commentaires sur le problème jouent un rôle de soutien dans l'application. La table Problèmes connexes vous permet de lier des problèmes. La table Commentaires sur le problème stocke plusieurs commentaires pour un même problème.</span><span class="sxs-lookup"><span data-stu-id="671cb-p105">The tables created by selecting the Issues schema are displayed in the Tile Pane. The Issues, Customer, and Employees tables are the main focus of the app. The Issues table stores information about each issue. Each issue is opened by and assigned to an employee on behalf of a customer. The Related Issues and Issue Comments tables play a supporting role in the app. The Related Issues table enables you to link one issue to another. The Issue Comments table stores multiple comments for a single issue.</span></span>
  
<span data-ttu-id="671cb-p106">Dans une base de données du bureau Access (.accdb), les relations entre tables sont gérées dans la fenêtre **Relations**. Les applications Access 2013 gèrent les relations à l'aide de champs définis pour le type de données **Recherche**. Examinons les relations pour la table Problèmes en cliquant avec le bouton droit sur l'élément de mosaïque **Problèmes**, puis en sélectionnant **Modifier la table**.</span><span class="sxs-lookup"><span data-stu-id="671cb-p106">In an Access desktop (.accdb) database, the relationships between tables are managed in the **Relationships** window. Access 2013 apps manage relationships by using fields set to the **Lookup** data type. Let's examine the relationships for the Issues table by right-clicking the **Issues** tile and selecting **Edit Table**.</span></span>
  
<span data-ttu-id="671cb-p107">Le champ **Client** est associé à la table **Clients**. Pour examiner la relation, sélectionnez le champ **Client**, puis **Modifier les listes de choix**. L' **Assistant Liste de choix** s'affiche comme illustré à la figure 2.</span><span class="sxs-lookup"><span data-stu-id="671cb-p107">The **Customer** field is related to the **Customers** table. To examine the relationship, select the **Customer** field and then select **Modify Lookups**. The **Lookup Wizard** is displayed, as shown in Figure 2.</span></span> 
  
<span data-ttu-id="671cb-144">**Figure 2. Assistant Liste de choix affichant la relation à la table Clients**</span><span class="sxs-lookup"><span data-stu-id="671cb-144">**Figure 2. Lookup Wizard displaying the relationship to the Customers table**</span></span>

<span data-ttu-id="671cb-145">![Assistant Liste de choix affichant la relation](media/odc_Access15_CreateAndCustomizeWebApp_Figure02.jpg "Assistant Liste de choix affichant la relation")</span><span class="sxs-lookup"><span data-stu-id="671cb-145">![Lookup Wizard displaying the relationship](media/odc_Access15_CreateAndCustomizeWebApp_Figure02.jpg "Lookup Wizard displaying the relationship")</span></span>
  
<span data-ttu-id="671cb-146">La boîte de dialogue de l'Assistant Liste de choix indique que le champ **Client** est lié à la table **Clients**, et invite à revenir au champ **Nom complet Prénom Nom** de la table **Clients**.</span><span class="sxs-lookup"><span data-stu-id="671cb-146">The Lookup Wizard dialog box shows that the **Customer** field is linked to the **Customers** table and to return the **Display Name First Last** field from the **Customers** table.</span></span> 
  
<span data-ttu-id="671cb-p108">Les champs **Ouvert par**, **Affecté à** et **Modifié par** ont trait à la table **Employés**. Plusieurs autres champs sont également définis pour le type de données **Recherche**. Dans ces cas, celui-ci est utilisé pour spécifier les valeurs à autoriser pour ce champ.</span><span class="sxs-lookup"><span data-stu-id="671cb-p108">The **Opened By**, **Assigned To**, and **Changed By** fields are related to the **Employees** table. Several other fields are also set to the **Lookup** data type. In these cases, the Lookup data type is used to specify the specific values to allow for in the field.</span></span> 
  
<span data-ttu-id="671cb-p109">Fermez la table **Problèmes**, puis examinez le volet des mosaïques. Les trois mosaïques supérieures pour les tables **Problèmes**, **Clients** et **Employés** s'affichent différemment des deux mosaïques inférieures pour les tables **Problèmes connexes** et **Commentaires sur le problème**, comme l'illustre la figure 3.</span><span class="sxs-lookup"><span data-stu-id="671cb-p109">Close the **Issues** table and examine the Tile Pane. The top three tiles, for the **Issues**, **Customers**, and **Employees** tables, are displayed differently than the bottom two tiles for the **Related Issues** and **Issue Comments** table, as shown in Figure 3.</span></span> 
  
<span data-ttu-id="671cb-152">**Figure 3. Volet des mosaïques pour le schéma Problèmes**</span><span class="sxs-lookup"><span data-stu-id="671cb-152">**Figure 3. Tile Pane for the Issues schema**</span></span>

<span data-ttu-id="671cb-153">![Volet des mosaïques pour le schéma Problèmes](media/odc_Access15_CreateAndCustomizeWebApp_Figure03.jpg "Volet des mosaïques pour le schéma Problèmes")</span><span class="sxs-lookup"><span data-stu-id="671cb-153">![Tile Pane for the Issues schema](media/odc_Access15_CreateAndCustomizeWebApp_Figure03.jpg "Tile Pane for the Issues schema")</span></span>
  
<span data-ttu-id="671cb-154">Les tables **Problèmes connexes** et **Commentaires sur le problème** sont grisées parce qu'elles devront être invisibles pour l'utilisateur dans le navigateur web.</span><span class="sxs-lookup"><span data-stu-id="671cb-154">The **Related Issues** and **Issue Comments** tables are dimmed because they are to be hidden from the user in the web browser.</span></span> 
  
<span data-ttu-id="671cb-p110">Utilisons l'application pour suivre certains problèmes. À cette fin, cliquez sur **Démarrer l'application** pour ouvrir l'application dans votre navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="671cb-p110">Let's use the app to track some issues. To do this, click **Launch App** to open the app in your web browser.</span></span> 
  
<span data-ttu-id="671cb-p111">L'application ouvre l'affichage **Liste des problèmes** de la table Problèmes. Avant d'ajouter un problème, il est recommande d'ajouter des clients et employés. Pour commencer à ajouter des clients, cliquez sur la mosaïque **Clients**.</span><span class="sxs-lookup"><span data-stu-id="671cb-p111">The app opens the **Issues List** view of the Issues table. Before adding an issue, it would be a good idea to add some customers and employees. Click the **Customers** tile to start adding customers.</span></span> 
  
<span data-ttu-id="671cb-160">Utilisez le Sélecteur d'affichage pour choisir l'un des trois modes d'affichage disponibles pour la table **Clients**, à savoir **Liste**, **Feuille de données** ou **Groupes**, comme illustré à la figure 4.</span><span class="sxs-lookup"><span data-stu-id="671cb-160">Use the View Selector to choose one of three views available for the **Customers** table, labeled **List**, **Datasheet**, and **Groups** as shown in Figure 4.</span></span> 
  
<span data-ttu-id="671cb-161">**Figure 4. Sélecteur d’affichage**</span><span class="sxs-lookup"><span data-stu-id="671cb-161">**Figure 4. View Selector**</span></span>

<span data-ttu-id="671cb-162">![Sélecteur d'affichage](media/odc_Access15_CreateAndCustomizeWebApp_Figure04.jpg "Sélecteur d'affichage")</span><span class="sxs-lookup"><span data-stu-id="671cb-162">![View Selector](media/odc_Access15_CreateAndCustomizeWebApp_Figure04.jpg "View Selector")</span></span>
  
<span data-ttu-id="671cb-p112">Le choix du mode **Liste** active l'affichage **Liste des clients**, qui est un affichage de type Détails de la liste. L'affichage Détails de la liste est l'un de ceux qu'Access génère automatiquement lors de la création d'une table. Le principal élément qui caractérise un affichage Détails de la liste est le volet Liste du côté gauche de l'affichage. Ce volet permet de filtrer et de parcourir les enregistrements figurant dans l'affichage. Dans une base de données du Bureau Access , l'implémentation d'un affichage Liste permettant d'effectuer une recherche requiert l'écriture d'un code personnalisé.</span><span class="sxs-lookup"><span data-stu-id="671cb-p112">Choosing **List** activates the **Customers List** view, which is a List Details view. List Details is one of the views Access automatically generates when you create a table. The main feature that distinguishes a List Details view is the list pane that appears on the left side of the view. The list pane is used to filter and navigate the records contained in the view. In an Access desktop database, implementing a searchable list view would require writing custom code.</span></span> 
  
<span data-ttu-id="671cb-p113">Le choix du mode **Feuille de données** ouvre l'affichage **Feuille de données clients**. La feuille de données est l'autre type d'affichage qu'Access génère automatiquement lors de la création d'une table. L'affichage Feuille de données est utile pour ceux qui trouvent plus facile d'entrer, de trier et de filtrer des données comme ils le font dans une feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="671cb-p113">Choosing **Datasheet** opens the **Customers Datasheet** view. Datasheet is the other kind of view Access automatically generates when you create a table. Datasheet views are useful for those who find it easier to enter, sort, and filter data in a spreadsheet-like manner.</span></span> 
  
<span data-ttu-id="671cb-p114">Le choix du mode Groupes ouvre un Affichage de synthèse. Ce type d'affichage permet de regrouper des enregistrements sur la base d'un champ, et d'éventuellement calculer une somme ou une moyenne.</span><span class="sxs-lookup"><span data-stu-id="671cb-p114">Choosing Groups opens a Summary view. Summary views can be used to group records based on a field and optionally calculate a sum or average.</span></span>
  
<span data-ttu-id="671cb-p115">Lors de l'ajout de clients, utilisez la barre d'action pour ajouter, modifier, rétablir, enregistrer ou supprimer des enregistrements. La barre d'action est une barre d'outils personnalisable qui s'affiche en haut de chaque affichage, comme l'illustre la figure 5.</span><span class="sxs-lookup"><span data-stu-id="671cb-p115">As you're adding customers, use the Action Bar to add records, edit records, save records, delete records, and cancel edits. The Action Bar is a customizable toolbar that appears at the top of each view, as shown in Figure 5.</span></span>
  
<span data-ttu-id="671cb-175">**Figure 5. Barre d’action**</span><span class="sxs-lookup"><span data-stu-id="671cb-175">**Figure 5. Action Bar**</span></span>

<span data-ttu-id="671cb-176">![Barre d’action](media/odc_Access15_CreateAndCustomizeWebApp_Figure05.jpg "Barre d’action")</span><span class="sxs-lookup"><span data-stu-id="671cb-176">![Action Bar](media/odc_Access15_CreateAndCustomizeWebApp_Figure05.jpg "Action Bar")</span></span>
  
<span data-ttu-id="671cb-p116">Après avoir ajouté des clients et des employés, ouvrez l'affichage Liste des problèmes, puis commencez à ajouter un problème. À mesure que vous tapez le nom d'un client dans le champ Client, un ou plusieurs noms de client s'affichent, comme l'illustre la figure 6.</span><span class="sxs-lookup"><span data-stu-id="671cb-p116">Once you've added some customers and employees open the Issues List view and start adding an issue. As you type the name of a customer into the into the Customer box, one or more of the customer names will appear, as shown in Figure 6.</span></span>
  
<span data-ttu-id="671cb-179">**Figure 6. Contrôle de saisie semi-automatique**</span><span class="sxs-lookup"><span data-stu-id="671cb-179">**Figure 6. AutoComplete control**</span></span>

<span data-ttu-id="671cb-180">![Contrôle de saisie semi-automatique](media/odc_Access15_CreateAndCustomizeWebApp_Figure06.jpg "Contrôle de saisie semi-automatique")</span><span class="sxs-lookup"><span data-stu-id="671cb-180">![AutoComplete control](media/odc_Access15_CreateAndCustomizeWebApp_Figure06.jpg "AutoComplete control")</span></span>
  
<span data-ttu-id="671cb-p117">Le champ Client est un contrôle de saisie semi-automatique. Ce contrôle affiche la liste des enregistrements correspondant à ce que vous tapez dans le champ. Cela vous aide à contrôler l'exactitude des données que vous entrez.</span><span class="sxs-lookup"><span data-stu-id="671cb-p117">The Customer box is an AutoComplete control. The AutoComplete control displays a list of records that match what you're typing into the box. This helps ensure the accuracy of data entry.</span></span>
  
## <a name="customize-the-app"></a><span data-ttu-id="671cb-184">Personnalisation de l'application</span><span class="sxs-lookup"><span data-stu-id="671cb-184">Customize the app</span></span>
<span data-ttu-id="671cb-185"><a name="ac15_CreateAndCustomizeWebApp_CustomizeTheApp"> </a></span><span class="sxs-lookup"><span data-stu-id="671cb-185"><a name="ac15_CreateAndCustomizeWebApp_CustomizeTheApp"> </a></span></span>

<span data-ttu-id="671cb-p118">Après avoir examiné l'application, vous constatez que l'affichage Liste des problèmes ne contient pas d'information de contact pour le client. Personnalisons l'application pour ajouter le numéro de téléphone professionnel du client à la table Problème lors de la création d'un problème.</span><span class="sxs-lookup"><span data-stu-id="671cb-p118">Now that you've taken a tour of the app, you notice that the Issues List view doesn't contain contact information for the customer. Let's customize the app to add the customer's work phone to the Issues table as the issue is being created.</span></span>
  
### <a name="to-add-a-field-to-the-issues-table"></a><span data-ttu-id="671cb-188">Pour ajouter un champ à la table Problèmes</span><span class="sxs-lookup"><span data-stu-id="671cb-188">To add a field to the Issues table</span></span>

1. <span data-ttu-id="671cb-189">Ouvrez l'application dans Access.</span><span class="sxs-lookup"><span data-stu-id="671cb-189">Open the app in Access.</span></span>
    
2. <span data-ttu-id="671cb-190">Sélectionnez la mosaïque **Problèmes**, l'icône **Paramètres/Action**, puis **Modifier la table**.</span><span class="sxs-lookup"><span data-stu-id="671cb-190">Choose the **Issues** tile, choose the **Settings/Action** icon, and then choose **Edit Table**.</span></span>
    
3. <span data-ttu-id="671cb-191">Entrez les **Coordonnées du contact** dans la première cellule vide de la colonne **Nom de champ**.</span><span class="sxs-lookup"><span data-stu-id="671cb-191">Enter **Contact Number** in the first blank cell in the **Field Name** column.</span></span> 
    
4. <span data-ttu-id="671cb-192">Sélectionnez **Texte court** dans la colonne **Type de données**.</span><span class="sxs-lookup"><span data-stu-id="671cb-192">Choose **Short Text** in the **Data Type** column.</span></span> 
    
5. <span data-ttu-id="671cb-193">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="671cb-193">Choose **Save**.</span></span>
    
6. <span data-ttu-id="671cb-194">Fermez la table Problèmes.</span><span class="sxs-lookup"><span data-stu-id="671cb-194">Close the Issues table.</span></span>
    
<span data-ttu-id="671cb-195">À présent que nous avons un champ dans lequel enregistrer le numéro de téléphone, créons une macro de données pour rechercher les informations de contact.</span><span class="sxs-lookup"><span data-stu-id="671cb-195">Now that we have field in which to store the phone number, let's create a data macro to look up the contact information.</span></span>
  
### <a name="to-create-the-data-macro-to-look-up-contact-information"></a><span data-ttu-id="671cb-196">Pour créer la macro de données recherchant des informations de contact</span><span class="sxs-lookup"><span data-stu-id="671cb-196">To create the data macro to look up contact information</span></span>

1. <span data-ttu-id="671cb-197">Dans le groupe **Créer**, sélectionnez **Avancé**, puis **Macro de données**.</span><span class="sxs-lookup"><span data-stu-id="671cb-197">In the **Create** group, choose **Advanced**, and then choose **Data Macro**.</span></span>
    
2. <span data-ttu-id="671cb-198">Sélectionnez **Créer un paramètre**.</span><span class="sxs-lookup"><span data-stu-id="671cb-198">Choose **Create Parameter**.</span></span>
    
3. <span data-ttu-id="671cb-p119">Dans le champ **Nom**, entrez **CustID**. Dans la liste déroulante **Type**, sélectionnez **Nombre (décimale flottante).**</span><span class="sxs-lookup"><span data-stu-id="671cb-p119">In the **Name** box, enter **CustID**. In the **Type** dropdown, choose **Number (Floating Decimal).**</span></span>
    
4. <span data-ttu-id="671cb-201">Dans la liste déroulante **Ajouter une nouvelle action**, sélectionnez **LookupRecord**.</span><span class="sxs-lookup"><span data-stu-id="671cb-201">From the **Add New Action** dropdown, choose **LookupRecord**.</span></span> 
    
5. <span data-ttu-id="671cb-202">Dans la liste déroulante **Rechercher un enregistrement dans**, sélectionnez **Clients**.</span><span class="sxs-lookup"><span data-stu-id="671cb-202">In the **Look Up A Record In** dropdown, choose **Customers**.</span></span> 
    
6. <span data-ttu-id="671cb-203">Dans le champ **Condition Where**, entrez **[Customers].[ID]=[CustID]**.</span><span class="sxs-lookup"><span data-stu-id="671cb-203">In the **Where Condition** box, enter **[Customers].[ID]=[CustID]**.</span></span> 
    
7. <span data-ttu-id="671cb-204">Dans la liste déroulante **Ajouter une nouvelle Action**, sélectionnez **SetReturnVar**.</span><span class="sxs-lookup"><span data-stu-id="671cb-204">Choose **SetReturnVar** from the **Add New Action** dropdown.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="671cb-205">Vous verrez deux listes déroulantes **Ajouter une nouvelle action** : une au sein du bloc **LookupRecord** et une autre extérieure au bloc **LookupRecord**.</span><span class="sxs-lookup"><span data-stu-id="671cb-205">You'll see two **Add New Action** dropdowns, one within the **LookupRecord** block, and another outside the **LookupRecord** block.</span></span> <span data-ttu-id="671cb-206">Vous devez sélectionner la liste déroulante **Ajouter une nouvelle action** dans le bloc **LookupRecord**, comme illustré dans la Figure 7.</span><span class="sxs-lookup"><span data-stu-id="671cb-206">You should choose the **Add New Action** dropdown within the **LookupRecord** block, as shown in Figure 7.</span></span> 
  
   <span data-ttu-id="671cb-207">**Figure 7. Liste déroulante Ajouter une nouvelle action**</span><span class="sxs-lookup"><span data-stu-id="671cb-207">**Figure 7. Add New Action dropdown**</span></span>

   <span data-ttu-id="671cb-208">![Liste déroulante Ajouter une nouvelle Action](media/odc_Access15_CreateAndCustomizeWebApp_Figure07.jpg "Liste déroulante Ajouter une nouvelle action")</span><span class="sxs-lookup"><span data-stu-id="671cb-208">![Add New Action dropdown](media/odc_Access15_CreateAndCustomizeWebApp_Figure07.jpg "Add New Action dropdown")</span></span>
  
8. <span data-ttu-id="671cb-209">Dans le champ **Nom**, entrez **TéléphoneContact**.</span><span class="sxs-lookup"><span data-stu-id="671cb-209">In the **Name** box, enter **ContactPhone**.</span></span> 
    
9. <span data-ttu-id="671cb-210">Dans le champ **Expression**, entrez **[Customers].[Work Phone]**.</span><span class="sxs-lookup"><span data-stu-id="671cb-210">In the **Expression** box, enter **[Customers].[Work Phone]**.</span></span> 
    
10. <span data-ttu-id="671cb-p121">Sélectionnez **Enregistrer**. Dans le champ **Nom de macro**, entrez **ObtenirTéléphoneContact**, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="671cb-p121">Choose **Save**. Enter **GetContactPhone** in the **Macro Name** box and then choose **OK**.</span></span>
    
    <span data-ttu-id="671cb-213">La macro doit ressembler celle illustrée à la figure 8.</span><span class="sxs-lookup"><span data-stu-id="671cb-213">The macro should resemble the macro shown in Figure 8.</span></span>
    
    <span data-ttu-id="671cb-214">**Figure 8. Macro de données ObtenirTéléphoneContact**</span><span class="sxs-lookup"><span data-stu-id="671cb-214">**Figure 8. GetContactPhone data macro**</span></span>

    <span data-ttu-id="671cb-215">![Macro de données ObtenirTéléphoneContact](media/odc_Access15_CreateAndCustomizeWebApp_Figure08.jpg "Macro de données ObtenirTéléphoneContact")</span><span class="sxs-lookup"><span data-stu-id="671cb-215">![GetContactPhone data macro](media/odc_Access15_CreateAndCustomizeWebApp_Figure08.jpg "GetContactPhone data macro")</span></span>
  
11. <span data-ttu-id="671cb-216">Fermez l'affichage Création de macros.</span><span class="sxs-lookup"><span data-stu-id="671cb-216">Close macro Design View.</span></span>
    
<span data-ttu-id="671cb-217">À présent, nous sommes prêts à ajouter le champ **Coordonnées du contact** au formulaire Liste des problèmes.</span><span class="sxs-lookup"><span data-stu-id="671cb-217">Now we're ready to add the **Contact Number** field to the Issues List form.</span></span> 
  
### <a name="to-add-the-contact-number-field-to-the-issues-list-form"></a><span data-ttu-id="671cb-218">Pour ajouter le champ Coordonnées du contact au formulaire Liste des problèmes</span><span class="sxs-lookup"><span data-stu-id="671cb-218">To add the Contact Number field to the Issues List form</span></span>

1. <span data-ttu-id="671cb-p122">Sélectionnez la table **Problèmes**. Cette action sélectionne le formulaire Liste des problèmes.</span><span class="sxs-lookup"><span data-stu-id="671cb-p122">Choose the **Issues** table. This chooses the Issues list form.</span></span> 
    
2. <span data-ttu-id="671cb-221">Dans le sélecteur d'affichage, sélectionnez **Liste**, l'icône **Paramètres/Action**, puis **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="671cb-221">In the View selector, choose **List**, choose the **Settings/Action** icon, and then choose **Edit**.</span></span>
    
3. <span data-ttu-id="671cb-222">Faites glisser le champ **Cordonnées du contact** du volet **Liste de champs** vers l'emplacement du formulaire où vous voulez que le numéro de contact s'affiche.</span><span class="sxs-lookup"><span data-stu-id="671cb-222">Drag the **Contact Number** field form the **Field List** pane to the location on the form where you want the contact number to be displayed.</span></span> 
    
4. <span data-ttu-id="671cb-223">Activez la case à cocher **Coordonnées du contact**, puis cliquez sur **Données**.</span><span class="sxs-lookup"><span data-stu-id="671cb-223">Choose the **Contact Number** text box, and then click **Data**.</span></span> 
    
5. <span data-ttu-id="671cb-224">Dans le champ **Nom du contrôle**, entrez **ContactClient**, puis fermez la fenêtre contextuelle **Données**.</span><span class="sxs-lookup"><span data-stu-id="671cb-224">In the **Control Name** box, enter **CustomerContact** and then close the **Data** popup.</span></span> 
    
6. <span data-ttu-id="671cb-225">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="671cb-225">Choose **Save**.</span></span>
    
<span data-ttu-id="671cb-p123">À présent, nous devons écrire une macro d'interface utilisateur qui copie le champ **Téléphone professionnel** de la table **Clients** vers le champ **Téléphone du contact** de la table **Problèmes**. L'événement **Après la mise à jour** du contrôle **CustomerAutocomplete** est un bon emplacement pour enregistrer la macro.</span><span class="sxs-lookup"><span data-stu-id="671cb-p123">Now we should write a user interface (UI) macro that copies the **Work Phone** field from the **Customers** table into the **Contact Phone** field of the **Issues** table. The **After Update** event of the **CustomerAutocomplete** control is a good location for the macro.</span></span> 
  
### <a name="to-create-the-afterupdate-macro"></a><span data-ttu-id="671cb-228">Pour créer la macro AprèsMiseàJour</span><span class="sxs-lookup"><span data-stu-id="671cb-228">To create the AfterUpdate macro</span></span>

1. <span data-ttu-id="671cb-229">Sélectionnez le contrôle **CustomerAutocomplete**, le bouton **Actions**, puis **Après la mise à jour**.</span><span class="sxs-lookup"><span data-stu-id="671cb-229">Choose the **CustomerAutocomplete** control, choose the **Actions** button, and then choose **After Update**.</span></span> 
    
    <span data-ttu-id="671cb-230">Une macro vide s'ouvre dans l'affichage Création de macros.</span><span class="sxs-lookup"><span data-stu-id="671cb-230">A blank macro is opened in macro Design View.</span></span>
    
2. <span data-ttu-id="671cb-231">Dans la liste déroulante **Ajouter une nouvelle action**, sélectionnez **ExécuterMacroDonnées**.</span><span class="sxs-lookup"><span data-stu-id="671cb-231">From the **Add New Action** dropdown, choose **RunDataMacro**.</span></span> 
    
3. <span data-ttu-id="671cb-232">Dans la liste déroulante **Nom de la macro**, sélectionnez **ObtenirTéléphoneContact**.</span><span class="sxs-lookup"><span data-stu-id="671cb-232">In the **Macro Name** dropdown, choose **GetContactPhone**.</span></span> 
    
4. <span data-ttu-id="671cb-233">Dans le champ **CustID**, entrez **[CustomerAutocomplete]**.</span><span class="sxs-lookup"><span data-stu-id="671cb-233">In the **CustID** box, enter **[CustomerAutocomplete]**.</span></span> 
    
5. <span data-ttu-id="671cb-234">Dans le champ **DéfinirVarLocale**, entrez **Téléphone**.</span><span class="sxs-lookup"><span data-stu-id="671cb-234">In the **SetLocalVar** box, enter **Phone**.</span></span> 
    
    <span data-ttu-id="671cb-235">Après sélection de la macro de données ObtenirTéléphoneContact créée précédemment, Access a automatiquement complété le nom du paramètre et renvoie une variable pour la macro.</span><span class="sxs-lookup"><span data-stu-id="671cb-235">When you chose the GetContactPhone data macro that was created earlier, Access automatically filled in the parameter name and return variable for the macro.</span></span>
    
    <span data-ttu-id="671cb-236">Le numéro de téléphone du client est stocké dans une variable nommée Téléphone.</span><span class="sxs-lookup"><span data-stu-id="671cb-236">The phone number for the customer is stored in a variable named Phone.</span></span>
    
6. <span data-ttu-id="671cb-237">Dans la liste déroulante **Ajouter une nouvelle action**, sélectionnez **DéfinirPropriété**.</span><span class="sxs-lookup"><span data-stu-id="671cb-237">From the **Add New Action** dropdown, choose **SetProperty**.</span></span> 
    
7. <span data-ttu-id="671cb-238">Dans le champ **Nom du contrôle**, entrez **ContactClient**.</span><span class="sxs-lookup"><span data-stu-id="671cb-238">In the **Control Name** box, enter **CustomerContact**.</span></span> 
    
8. <span data-ttu-id="671cb-239">Dans la liste déroulante **Propriété**, sélectionnez **Valeur**.</span><span class="sxs-lookup"><span data-stu-id="671cb-239">In the **Property** dropdown, choose **Value**.</span></span> 
    
9. <span data-ttu-id="671cb-240">Dans le champ **Valeur**, entrez **=[Phone]**.</span><span class="sxs-lookup"><span data-stu-id="671cb-240">In the **Value** box, enter **=[Phone]**.</span></span> 
    
10. <span data-ttu-id="671cb-241">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="671cb-241">Choose **Save**.</span></span>
    
    <span data-ttu-id="671cb-242">La macro doit ressembler celle illustrée à la figure 9.</span><span class="sxs-lookup"><span data-stu-id="671cb-242">The macro should resemble the macro shown in Figure 9.</span></span>
    
    <span data-ttu-id="671cb-243">**Figure 9. Macro Après mise à jour**</span><span class="sxs-lookup"><span data-stu-id="671cb-243">**Figure 9. After Update macro**</span></span>

    <span data-ttu-id="671cb-244">![Macro Après mise à jour](media/odc_Access15_CreateAndCustomizeWebApp_Figure09.jpg "Macro Après mise à jour")</span><span class="sxs-lookup"><span data-stu-id="671cb-244">![After Update macro](media/odc_Access15_CreateAndCustomizeWebApp_Figure09.jpg "After Update macro")</span></span>
  
11. <span data-ttu-id="671cb-245">Fermez l'affichage Création de macros.</span><span class="sxs-lookup"><span data-stu-id="671cb-245">Close macro Design View.</span></span>
    
12. <span data-ttu-id="671cb-p124">Fermez l'affichage Liste des problèmes. Lorsque vous êtes invité à enregistrer vos modifications, sélectionnez **Oui**.</span><span class="sxs-lookup"><span data-stu-id="671cb-p124">Close the Issues List view. Choose **Yes** when you are prompted to save your changes.</span></span> 
    
<span data-ttu-id="671cb-248">À présent, nous sommes prêts pour la personnalisation du texte.</span><span class="sxs-lookup"><span data-stu-id="671cb-248">Now we're ready to text the customization.</span></span> <span data-ttu-id="671cb-249">Cliquez sur **Lancer l’application** pour ouvrir l’application dans votre navigateur web, puis ajoutez un problème.</span><span class="sxs-lookup"><span data-stu-id="671cb-249">Click **Launch App** to open the app in your web browser and then add a new issue.</span></span> <span data-ttu-id="671cb-250">Le champ **Coordonnées du contact** est automatiquement mis à jour après la saisie du nom du client, comme illustré à la Figure 10.</span><span class="sxs-lookup"><span data-stu-id="671cb-250">The **Contact Number** box updates automatically after the customer name is entered,  as shown in Figure 10.</span></span> 
  
<span data-ttu-id="671cb-251">**Figure 10. Affichage Problèmes mis à jour avec un numéro de téléphone**</span><span class="sxs-lookup"><span data-stu-id="671cb-251">**Figure 10. Issues view updated with phone number**</span></span>

<span data-ttu-id="671cb-252">![Affichage Problèmes mis à jour avec un numéro de téléphone](media/odc_Access15_CreateAndCustomizeWebApp_Figure10.jpg "Affichage Problèmes mis à jour avec un numéro de téléphone")</span><span class="sxs-lookup"><span data-stu-id="671cb-252">![Issues view updated with phone number](media/odc_Access15_CreateAndCustomizeWebApp_Figure10.jpg "Issues view updated with phone number")</span></span>
  
## <a name="conclusion"></a><span data-ttu-id="671cb-253">Conclusion</span><span class="sxs-lookup"><span data-stu-id="671cb-253">Conclusion</span></span>

<span data-ttu-id="671cb-p126">L'utilisation d'un des modèles de schéma inclus dans est une bonne manière de commencer à créer une application web Access. Les affichages créés automatiquement pour vous contiennent des fonctionnalités avancées qui requièrent un code personnalisé à implémenter dans une base de données du Bureau Access.</span><span class="sxs-lookup"><span data-stu-id="671cb-p126">Using one of the schema templates included with is a good way to jump start the creation of an Access web app. The views that are automatically created for you contain advanced functionally that requires custom code to implement in a Access desktop database.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="671cb-256">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="671cb-256">See also</span></span>

- [<span data-ttu-id="671cb-257">Nouveautés d’Access 2013 pour les développeurs</span><span class="sxs-lookup"><span data-stu-id="671cb-257">What's new for Access 2013 developers</span></span>](https://msdn.microsoft.com/library/df778f51-d65e-4c30-b618-65003ceb39b3%28Office.15%29.aspx) 
- [<span data-ttu-id="671cb-258">Référence de l'application web personnalisée Access</span><span class="sxs-lookup"><span data-stu-id="671cb-258">Access custom web app reference</span></span>](access-custom-web-app-reference.md)
  

