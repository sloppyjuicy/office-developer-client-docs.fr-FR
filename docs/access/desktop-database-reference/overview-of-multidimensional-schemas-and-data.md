---
title: Présentation des schémas et données multidimensionnels
TOCTitle: Overview of Multidimensional Schemas and Data
ms:assetid: a963e993-b7bf-eeb4-ecd5-d6fe43cf4bb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249784(v=office.15)
ms:contentKeyID: 48546923
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 376d80bc79af772cfd09b6f5b8759321ed4431ee
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887165"
---
# <a name="overview-of-multidimensional-schemas-and-data"></a><span data-ttu-id="b6d36-102">Présentation des schémas et données multidimensionnels</span><span class="sxs-lookup"><span data-stu-id="b6d36-102">Overview of Multidimensional Schemas and Data</span></span>


<span data-ttu-id="b6d36-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b6d36-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="b6d36-104">Présentation des schémas multidimensionnels</span><span class="sxs-lookup"><span data-stu-id="b6d36-104">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="b6d36-105">Dans ADO MD, l'objet de métadonnées central est le *cube*, qui consiste en un ensemble structuré de dimensions, hiérarchies, niveaux et membres connexes.</span><span class="sxs-lookup"><span data-stu-id="b6d36-105">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="b6d36-106">Une *dimension* est une catégorie indépendante de données à partir de votre base de données multidimensionnelle sur vos entités professionnelles.</span><span class="sxs-lookup"><span data-stu-id="b6d36-106">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities.</span></span> <span data-ttu-id="b6d36-107">En règle générale, une dimension contient les éléments à utiliser comme critères de requête pour les mesures de la base de données.</span><span class="sxs-lookup"><span data-stu-id="b6d36-107">A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="b6d36-108">Une *hiérarchie* est un chemin d’agrégation dans une dimension.</span><span class="sxs-lookup"><span data-stu-id="b6d36-108">A *hierarchy* is a path of aggregation of a dimension.</span></span> <span data-ttu-id="b6d36-109">Une dimension peut avoir plusieurs niveaux de granularité dotés de relations parent-enfant.</span><span class="sxs-lookup"><span data-stu-id="b6d36-109">A dimension may have multiple levels of granularity, which have parent-child relationships.</span></span> <span data-ttu-id="b6d36-110">Une hiérarchie permet de définir les relations entre ces niveaux.</span><span class="sxs-lookup"><span data-stu-id="b6d36-110">A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="b6d36-111">Un *niveau* est une étape d’agrégation dans une hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="b6d36-111">A *level* is a step of aggregation in a hierarchy.</span></span> <span data-ttu-id="b6d36-112">Pour les dimensions dotées de plusieurs couches d'informations, chaque couche constitue un niveau.</span><span class="sxs-lookup"><span data-stu-id="b6d36-112">For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="b6d36-113">Un *membre* est un élément de données dans une dimension.</span><span class="sxs-lookup"><span data-stu-id="b6d36-113">A *member* is a data item in a dimension.</span></span> <span data-ttu-id="b6d36-114">En règle générale, vous créez une légende ou décrivez une mesure de la base de données à l'aide de membres.</span><span class="sxs-lookup"><span data-stu-id="b6d36-114">Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="b6d36-p105">Les cubes sont représentés par des objets [CubeDef](cubedef-object-ado-md.md) dans ADO MD. Les dimensions, hiérarchies, niveaux et membres sont également représentés par leurs objets ADO MD correspondants : [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md) et [Member](member-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="b6d36-p105">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD. Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="b6d36-117">Dimensions</span><span class="sxs-lookup"><span data-stu-id="b6d36-117">Dimensions</span></span>

<span data-ttu-id="b6d36-p106">Les dimensions d'un cube dépendent de vos entités professionnelles et des types de données à représenter dans la base de données. En règle générale, chaque dimension constitue un point d'entrée ou un mécanisme indépendant permettant de sélectionner des données.</span><span class="sxs-lookup"><span data-stu-id="b6d36-p106">The dimensions of a cube depend on your business entities and types of data to be modeled in the database. Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="b6d36-p107">Par exemple, un cube contenant des données de ventes possède les cinq dimensions suivantes : Vendeur, Géographie, Heure, Produits et Mesures. La dimension Mesures contient les valeurs de données de ventes réelles tandis que les autres dimensions constituent des manières de classer et regrouper les valeurs des données de ventes.</span><span class="sxs-lookup"><span data-stu-id="b6d36-p107">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures. The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="b6d36-122">La dimension Géographie est constituée des membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b6d36-122">The Geography dimension has the following set of members:</span></span>

```text
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="b6d36-123">Hiérarchies</span><span class="sxs-lookup"><span data-stu-id="b6d36-123">Hierarchies</span></span>

<span data-ttu-id="b6d36-p108">Les hiérarchies définissent les manières de regrouper ou de reporter les niveaux d'une dimension. Une dimension peut compter plusieurs hiérarchies.</span><span class="sxs-lookup"><span data-stu-id="b6d36-p108">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped. A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="b6d36-126">Niveaux</span><span class="sxs-lookup"><span data-stu-id="b6d36-126">Levels</span></span>

<span data-ttu-id="b6d36-127">Dans l'exemple de la dimension Géographie de l'illustration précédente, chaque zone représente un niveau de la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="b6d36-127">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="b6d36-128">Chaque niveau est constitué de membres, comme suit :</span><span class="sxs-lookup"><span data-stu-id="b6d36-128">Each level has a set of members, as follows:</span></span>

  - <span data-ttu-id="b6d36-129">Monde = {All}
</span><span class="sxs-lookup"><span data-stu-id="b6d36-129">The World = {All}</span></span>

  - <span data-ttu-id="b6d36-130">Continents = {North America, Europe}
</span><span class="sxs-lookup"><span data-stu-id="b6d36-130">Continents = {North America, Europe}</span></span>

  - <span data-ttu-id="b6d36-131">Pays = {Canada, USA, UK, Germany}
</span><span class="sxs-lookup"><span data-stu-id="b6d36-131">Countries = {Canada, USA, UK, Germany}</span></span>

  - <span data-ttu-id="b6d36-132">Régions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}
</span><span class="sxs-lookup"><span data-stu-id="b6d36-132">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

  - <span data-ttu-id="b6d36-133">Villes = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}
</span><span class="sxs-lookup"><span data-stu-id="b6d36-133">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="b6d36-134">Membres</span><span class="sxs-lookup"><span data-stu-id="b6d36-134">Members</span></span>

<span data-ttu-id="b6d36-p109">Les membres inférieurs d'une hiérarchie n'ont pas d'enfants et les membres supérieurs n'ont pas de parents. Tous les autres membres ont au moins un parent et un enfant. Par exemple, une coupure transversale de l'arborescence hiérarchique de la dimension Géographie donne les relations parent-enfant suivantes :</span><span class="sxs-lookup"><span data-stu-id="b6d36-p109">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent. All other members have at least one parent and at least one child. For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

  - <span data-ttu-id="b6d36-138">{All} (parent) {Europe, Amérique du Nord}</span><span class="sxs-lookup"><span data-stu-id="b6d36-138">{All} (parent of) {Europe, North America}</span></span>

  - <span data-ttu-id="b6d36-139">{Amérique du Nord} (parent) {Canada, USA}</span><span class="sxs-lookup"><span data-stu-id="b6d36-139">{North America} (parent of) {Canada, USA}</span></span>

  - <span data-ttu-id="b6d36-140">{USA} (parent) {USA-NE, USA-NW, USA-SE, USA-SW}</span><span class="sxs-lookup"><span data-stu-id="b6d36-140">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>

  - <span data-ttu-id="b6d36-141">{USA-NW} (parent) {Seattle, Boise}</span><span class="sxs-lookup"><span data-stu-id="b6d36-141">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="b6d36-142">Les membres peuvent faire partie d'une ou plusieurs hiérachies par dimension.</span><span class="sxs-lookup"><span data-stu-id="b6d36-142">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="b6d36-p110">Cet exemple illustre également une autre caractéristique : certains membres du niveau Semaine de la hiérarchie Année-Semaine n'apparaissent dans aucun niveau de la hiérarchie Année-Trimestre. Autrement dit, une hiérarchie ne doit pas nécessairement comprendre tous les membres d'une dimension.</span><span class="sxs-lookup"><span data-stu-id="b6d36-p110">This example also illustrates another characteristic: Some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy. Thus, a hierarchy need not include all members of a dimension.</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="b6d36-145">Présentation des schémas multidimensionnels</span><span class="sxs-lookup"><span data-stu-id="b6d36-145">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="b6d36-146">Dans ADO MD, l'objet de métadonnées central est le *cube*, qui consiste en un ensemble structuré de dimensions, hiérarchies, niveaux et membres connexes.</span><span class="sxs-lookup"><span data-stu-id="b6d36-146">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="b6d36-147">Une *dimension* est une catégorie indépendante de données à partir de votre base de données multidimensionnelle sur vos entités professionnelles.</span><span class="sxs-lookup"><span data-stu-id="b6d36-147">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities.</span></span> <span data-ttu-id="b6d36-148">En règle générale, une dimension contient les éléments à utiliser comme critères de requête pour les mesures de la base de données.</span><span class="sxs-lookup"><span data-stu-id="b6d36-148">A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="b6d36-149">Une *hiérarchie* est un chemin d’agrégation dans une dimension.</span><span class="sxs-lookup"><span data-stu-id="b6d36-149">A *hierarchy* is a path of aggregation of a dimension.</span></span> <span data-ttu-id="b6d36-150">Une dimension peut avoir plusieurs niveaux de granularité dotés de relations parent-enfant.</span><span class="sxs-lookup"><span data-stu-id="b6d36-150">A dimension may have multiple levels of granularity, which have parent-child relationships.</span></span> <span data-ttu-id="b6d36-151">Une hiérarchie permet de définir les relations entre ces niveaux.</span><span class="sxs-lookup"><span data-stu-id="b6d36-151">A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="b6d36-152">Un *niveau* est une étape d’agrégation dans une hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="b6d36-152">A *level* is a step of aggregation in a hierarchy.</span></span> <span data-ttu-id="b6d36-153">Pour les dimensions dotées de plusieurs couches d'informations, chaque couche constitue un niveau.</span><span class="sxs-lookup"><span data-stu-id="b6d36-153">For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="b6d36-154">Un *membre* est un élément de données dans une dimension.</span><span class="sxs-lookup"><span data-stu-id="b6d36-154">A *member* is a data item in a dimension.</span></span> <span data-ttu-id="b6d36-155">En règle générale, vous créez une légende ou décrivez une mesure de la base de données à l'aide de membres.</span><span class="sxs-lookup"><span data-stu-id="b6d36-155">Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="b6d36-p115">Les cubes sont représentés par des objets [CubeDef](cubedef-object-ado-md.md) dans ADO MD. Les dimensions, hiérarchies, niveaux et membres sont également représentés par leurs objets ADO MD correspondants : [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md) et [Member](member-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="b6d36-p115">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD. Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="b6d36-158">Dimensions</span><span class="sxs-lookup"><span data-stu-id="b6d36-158">Dimensions</span></span>

<span data-ttu-id="b6d36-p116">Les dimensions d'un cube dépendent de vos entités professionnelles et des types de données à représenter dans la base de données. En règle générale, chaque dimension constitue un point d'entrée ou un mécanisme indépendant permettant de sélectionner des données.</span><span class="sxs-lookup"><span data-stu-id="b6d36-p116">The dimensions of a cube depend on your business entities and types of data to be modeled in the database. Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="b6d36-p117">Par exemple, un cube contenant des données de ventes possède les cinq dimensions suivantes : Vendeur, Géographie, Heure, Produits et Mesures. La dimension Mesures contient les valeurs de données de ventes réelles tandis que les autres dimensions constituent des manières de classer et regrouper les valeurs des données de ventes.</span><span class="sxs-lookup"><span data-stu-id="b6d36-p117">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures. The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="b6d36-163">La dimension Géographie est constituée des membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b6d36-163">The Geography dimension has the following set of members:</span></span>

```text 
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="b6d36-164">Hiérarchies</span><span class="sxs-lookup"><span data-stu-id="b6d36-164">Hierarchies</span></span>

<span data-ttu-id="b6d36-p118">Les hiérarchies définissent les manières de regrouper ou de reporter les niveaux d'une dimension. Une dimension peut compter plusieurs hiérarchies.</span><span class="sxs-lookup"><span data-stu-id="b6d36-p118">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped. A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="b6d36-167">Niveaux</span><span class="sxs-lookup"><span data-stu-id="b6d36-167">Levels</span></span>

<span data-ttu-id="b6d36-168">Dans l'exemple de la dimension Géographie de l'illustration précédente, chaque zone représente un niveau de la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="b6d36-168">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="b6d36-169">Chaque niveau est constitué de membres, comme suit :</span><span class="sxs-lookup"><span data-stu-id="b6d36-169">Each level has a set of members, as follows:</span></span>

- <span data-ttu-id="b6d36-170">Monde = {All}
</span><span class="sxs-lookup"><span data-stu-id="b6d36-170">The World = {All}</span></span>

- <span data-ttu-id="b6d36-171">Continents = {North America, Europe}
</span><span class="sxs-lookup"><span data-stu-id="b6d36-171">Continents = {North America, Europe}</span></span>

- <span data-ttu-id="b6d36-172">Pays = {Canada, USA, UK, Germany}
</span><span class="sxs-lookup"><span data-stu-id="b6d36-172">Countries = {Canada, USA, UK, Germany}</span></span>

- <span data-ttu-id="b6d36-173">Régions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}
</span><span class="sxs-lookup"><span data-stu-id="b6d36-173">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

- <span data-ttu-id="b6d36-174">Villes = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}
</span><span class="sxs-lookup"><span data-stu-id="b6d36-174">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="b6d36-175">Membres</span><span class="sxs-lookup"><span data-stu-id="b6d36-175">Members</span></span>

<span data-ttu-id="b6d36-p119">Les membres inférieurs d'une hiérarchie n'ont pas d'enfants et les membres supérieurs n'ont pas de parents. Tous les autres membres ont au moins un parent et un enfant. Par exemple, une coupure transversale de l'arborescence hiérarchique de la dimension Géographie donne les relations parent-enfant suivantes :</span><span class="sxs-lookup"><span data-stu-id="b6d36-p119">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent. All other members have at least one parent and at least one child. For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

- <span data-ttu-id="b6d36-179">{All} (parent) {Europe, Amérique du Nord}</span><span class="sxs-lookup"><span data-stu-id="b6d36-179">{All} (parent of) {Europe, North America}</span></span>

- <span data-ttu-id="b6d36-180">{Amérique du Nord} (parent) {Canada, USA}</span><span class="sxs-lookup"><span data-stu-id="b6d36-180">{North America} (parent of) {Canada, USA}</span></span>

- <span data-ttu-id="b6d36-181">{USA} (parent) {USA-NE, USA-NW, USA-SE, USA-SW}</span><span class="sxs-lookup"><span data-stu-id="b6d36-181">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>

- <span data-ttu-id="b6d36-182">{USA-NW} (parent) {Seattle, Boise}</span><span class="sxs-lookup"><span data-stu-id="b6d36-182">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="b6d36-183">Les membres peuvent faire partie d'une ou plusieurs hiérachies par dimension.</span><span class="sxs-lookup"><span data-stu-id="b6d36-183">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="b6d36-p120">Cet exemple illustre également une autre caractéristique : certains membres du niveau Semaine de la hiérarchie Année-Semaine n'apparaissent dans aucun niveau de la hiérarchie Année-Trimestre. Autrement dit, une hiérarchie ne doit pas nécessairement comprendre tous les membres d'une dimension.</span><span class="sxs-lookup"><span data-stu-id="b6d36-p120">This example also illustrates another characteristic: Some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy. Thus, a hierarchy need not include all members of a dimension.</span></span>

