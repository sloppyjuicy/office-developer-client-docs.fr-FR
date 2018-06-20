---
title: Automatisation d’InfoPath à partir d’une application externe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath fournit automation d’application à partir du code écrit à l’aide de COM et script à l’aide des méthodes de l’objet Application et de la collection XDocuments.
ms.openlocfilehash: 0e3fcc50ec11f5fc8791d37144767bf0398ccda7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782249"
---
# <a name="automating-infopath-from-an-external-application"></a><span data-ttu-id="ec846-103">Automatisation d’InfoPath à partir d’une application externe</span><span class="sxs-lookup"><span data-stu-id="ec846-103">Automating InfoPath from an external application</span></span>

<span data-ttu-id="ec846-104">Microsoft InfoPath fournit automation d’application à partir du code écrit à l’aide de COM et script à l’aide des méthodes de l’objet **Application** et de la collection **XDocuments** .</span><span class="sxs-lookup"><span data-stu-id="ec846-104">Microsoft InfoPath provides application automation from code written using COM and script by using methods of the **Application** object and the **XDocuments** collection.</span></span> 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a><span data-ttu-id="ec846-105">Vue d’ensemble de l’Application et les objets XDocument</span><span class="sxs-lookup"><span data-stu-id="ec846-105">Overview of the Application and XDocument Objects</span></span>

<span data-ttu-id="ec846-106">L’objet **Application** contient les méthodes suivantes utilisées pour l’automation :</span><span class="sxs-lookup"><span data-stu-id="ec846-106">The **Application** object contains the following methods used for automation:</span></span> 
  
|<span data-ttu-id="ec846-107">**Méthode**</span><span class="sxs-lookup"><span data-stu-id="ec846-107">**Method**</span></span>|<span data-ttu-id="ec846-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="ec846-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ec846-109">**CacheSolution**</span><span class="sxs-lookup"><span data-stu-id="ec846-109">**CacheSolution**</span></span> <br/> |<span data-ttu-id="ec846-110">Examine le dans le cache et, si nécessaire, met à jour à partir de l’emplacement publié du modèle de formulaire.</span><span class="sxs-lookup"><span data-stu-id="ec846-110">Examines the in the cache and, if necessary, updates it from the published location of the form template.</span></span>  <br/> |
|<span data-ttu-id="ec846-111">**Quit**</span><span class="sxs-lookup"><span data-stu-id="ec846-111">**Quit**</span></span> <br/> |<span data-ttu-id="ec846-112">Quitte l’application Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="ec846-112">Quits the Microsoft Office InfoPath application.</span></span>  <br/> |
|<span data-ttu-id="ec846-113">**RegisterSolution**</span><span class="sxs-lookup"><span data-stu-id="ec846-113">**RegisterSolution**</span></span> <br/> |<span data-ttu-id="ec846-114">Installe le modèle de formulaire Microsoft Office InfoPath spécifié.</span><span class="sxs-lookup"><span data-stu-id="ec846-114">Installs the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
|<span data-ttu-id="ec846-115">**UnregisterSolution**</span><span class="sxs-lookup"><span data-stu-id="ec846-115">**UnregisterSolution**</span></span> <br/> |<span data-ttu-id="ec846-116">Désinstalle le modèle de formulaire Microsoft Office InfoPath spécifié.</span><span class="sxs-lookup"><span data-stu-id="ec846-116">Uninstalls the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
   
<span data-ttu-id="ec846-117">La collection **XDocuments** contient les méthodes suivantes qui peuvent être utilisés pour l’automatisation externe :</span><span class="sxs-lookup"><span data-stu-id="ec846-117">The **XDocuments** collection contains the following methods that can be used for external automation:</span></span> 
  
|<span data-ttu-id="ec846-118">**Méthode**</span><span class="sxs-lookup"><span data-stu-id="ec846-118">**Method**</span></span>|<span data-ttu-id="ec846-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="ec846-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ec846-120">Méthode **Close**</span><span class="sxs-lookup"><span data-stu-id="ec846-120">**Close** method</span></span>  <br/> |<span data-ttu-id="ec846-121">Ferme le formulaire Microsoft Office InfoPath spécifié.</span><span class="sxs-lookup"><span data-stu-id="ec846-121">Closes the specified Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="ec846-122">Méthode **New**</span><span class="sxs-lookup"><span data-stu-id="ec846-122">**New** method</span></span>  <br/> |<span data-ttu-id="ec846-123">Crée un nouveau formulaire Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="ec846-123">Creates a new Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="ec846-124">Méthode **NewFromSolution**</span><span class="sxs-lookup"><span data-stu-id="ec846-124">**NewFromSolution** method</span></span>  <br/> |<span data-ttu-id="ec846-125">Crée un nouveau formulaire Microsoft Office InfoPath basé sur le modèle de formulaire spécifié.</span><span class="sxs-lookup"><span data-stu-id="ec846-125">Creates a new Microsoft Office InfoPath form based on the specified form template.</span></span>  <br/> |
|<span data-ttu-id="ec846-126">Méthode **NewFromSolutionWithData**</span><span class="sxs-lookup"><span data-stu-id="ec846-126">**NewFromSolutionWithData** method</span></span>  <br/> |<span data-ttu-id="ec846-127">Crée un nouveau formulaire Microsoft Office InfoPath utilisant le modèle de formulaire et les données XML spécifié.</span><span class="sxs-lookup"><span data-stu-id="ec846-127">Creates a new Microsoft Office InfoPath form using the specified XML data and form template.</span></span>  <br/> |
|<span data-ttu-id="ec846-128">Méthode **Open**</span><span class="sxs-lookup"><span data-stu-id="ec846-128">**Open** method</span></span>  <br/> |<span data-ttu-id="ec846-129">Ouvre le formulaire Microsoft Office InfoPath spécifié.</span><span class="sxs-lookup"><span data-stu-id="ec846-129">Opens the specified Microsoft Office InfoPath form.</span></span>  <br/> |
   
<span data-ttu-id="ec846-130">Pour utiliser l’objet **Application** d’une application externe, vous utilisez la fonction **CreateObject** avec le ProgID de l’application InfoPath (« InfoPath.Application ») pour créer une variable objet qui représente l’application InfoPath.</span><span class="sxs-lookup"><span data-stu-id="ec846-130">To use the **Application** object from an external application, you use the **CreateObject** function with the ProgID of the InfoPath application ("InfoPath.Application") to create an object variable that represents the InfoPath application.</span></span> <span data-ttu-id="ec846-131">Vous pouvez ensuite utiliser la propriété **XDocuments** pour accéder à la collection **XDocuments** et ses méthodes pour ouvrir ou créer un formulaire InfoPath.</span><span class="sxs-lookup"><span data-stu-id="ec846-131">You can then use the **XDocuments** property to access the **XDocuments** collection and use its methods to open or create an InfoPath form.</span></span> <span data-ttu-id="ec846-132">L’exemple suivant illustre la création d’une référence à l’objet **d’Application** à l’aide de Microsoft Visual Basic 6.0 ou Visual Basic pour Applications (VBA) langage de programmation :</span><span class="sxs-lookup"><span data-stu-id="ec846-132">The following example demonstrates the creation of a reference to the **Application** object using the Microsoft Visual Basic 6.0 or Visual Basic for Applications (VBA) programming language:</span></span> 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> <span data-ttu-id="ec846-133">Étant donné que la fonction **CreateObject** crée une variable d’objet à l’aide de la liaison tardive, la saisie semi-automatique ne sera pas disponible dans Visual Basic Editor.</span><span class="sxs-lookup"><span data-stu-id="ec846-133">Because the **CreateObject** function creates an object variable using late binding, automatic statement completion will not be available in the Visual Basic Editor.</span></span> <span data-ttu-id="ec846-134">Consultez les liens dans les tableaux ci-dessus pour plus d’informations sur la syntaxe d’appel correcte.</span><span class="sxs-lookup"><span data-stu-id="ec846-134">Refer to the links in the preceding tables for information about the correct calling syntax.</span></span> 
  

