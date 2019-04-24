---
title: Automatisation d’InfoPath à partir d’une application externe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath fournit l'automatisation des applications à partir du code écrit à l'aide de COM et du script à l'aide de méthodes de l'objet application et de la collection XDocuments.
ms.openlocfilehash: 7eccbca34b93aff7909de92eebc04d012d4dd97c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303807"
---
# <a name="automating-infopath-from-an-external-application"></a><span data-ttu-id="aeb40-103">Automatisation d’InfoPath à partir d’une application externe</span><span class="sxs-lookup"><span data-stu-id="aeb40-103">Automating InfoPath from an external application</span></span>

<span data-ttu-id="aeb40-104">Microsoft InfoPath fournit l'automatisation des applications à partir du code écrit à l'aide de COM et du script à l'aide de méthodes de l'objet **application** et de la collection **XDocuments** .</span><span class="sxs-lookup"><span data-stu-id="aeb40-104">Microsoft InfoPath provides application automation from code written using COM and script by using methods of the **Application** object and the **XDocuments** collection.</span></span> 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a><span data-ttu-id="aeb40-105">Vue d'ensemble des objets application et XDocument</span><span class="sxs-lookup"><span data-stu-id="aeb40-105">Overview of the Application and XDocument Objects</span></span>

<span data-ttu-id="aeb40-106">L'objet **application** contient les méthodes suivantes utilisées pour Automation:</span><span class="sxs-lookup"><span data-stu-id="aeb40-106">The **Application** object contains the following methods used for automation:</span></span> 
  
|<span data-ttu-id="aeb40-107">**Méthode**</span><span class="sxs-lookup"><span data-stu-id="aeb40-107">**Method**</span></span>|<span data-ttu-id="aeb40-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="aeb40-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aeb40-109">**CacheSolution**</span><span class="sxs-lookup"><span data-stu-id="aeb40-109">**CacheSolution**</span></span> <br/> |<span data-ttu-id="aeb40-110">Examine le dans le cache et, si nécessaire, le met à jour à partir de l'emplacement publié du modèle de formulaire.</span><span class="sxs-lookup"><span data-stu-id="aeb40-110">Examines the in the cache and, if necessary, updates it from the published location of the form template.</span></span>  <br/> |
|<span data-ttu-id="aeb40-111">**Quit**</span><span class="sxs-lookup"><span data-stu-id="aeb40-111">**Quit**</span></span> <br/> |<span data-ttu-id="aeb40-112">Quitte l'application Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="aeb40-112">Quits the Microsoft Office InfoPath application.</span></span>  <br/> |
|<span data-ttu-id="aeb40-113">**RegisterSolution**</span><span class="sxs-lookup"><span data-stu-id="aeb40-113">**RegisterSolution**</span></span> <br/> |<span data-ttu-id="aeb40-114">Installe le modèle de formulaire Microsoft Office InfoPath spécifié.</span><span class="sxs-lookup"><span data-stu-id="aeb40-114">Installs the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
|<span data-ttu-id="aeb40-115">**UnregisterSolution**</span><span class="sxs-lookup"><span data-stu-id="aeb40-115">**UnregisterSolution**</span></span> <br/> |<span data-ttu-id="aeb40-116">Désinstalle le modèle de formulaire Microsoft Office InfoPath spécifié.</span><span class="sxs-lookup"><span data-stu-id="aeb40-116">Uninstalls the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
   
<span data-ttu-id="aeb40-117">La collection **XDocuments** contient les méthodes suivantes, qui peuvent être utilisées pour l'automatisation externe:</span><span class="sxs-lookup"><span data-stu-id="aeb40-117">The **XDocuments** collection contains the following methods that can be used for external automation:</span></span> 
  
|<span data-ttu-id="aeb40-118">**Méthode**</span><span class="sxs-lookup"><span data-stu-id="aeb40-118">**Method**</span></span>|<span data-ttu-id="aeb40-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="aeb40-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aeb40-120">Méthode **Close**</span><span class="sxs-lookup"><span data-stu-id="aeb40-120">**Close** method</span></span>  <br/> |<span data-ttu-id="aeb40-121">Ferme le formulaire Microsoft Office InfoPath spécifié.</span><span class="sxs-lookup"><span data-stu-id="aeb40-121">Closes the specified Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="aeb40-122">**New** , méthode</span><span class="sxs-lookup"><span data-stu-id="aeb40-122">**New** method</span></span>  <br/> |<span data-ttu-id="aeb40-123">Crée un formulaire Microsoft Office InfoPath.</span><span class="sxs-lookup"><span data-stu-id="aeb40-123">Creates a new Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="aeb40-124">**NewFromSolution** , méthode</span><span class="sxs-lookup"><span data-stu-id="aeb40-124">**NewFromSolution** method</span></span>  <br/> |<span data-ttu-id="aeb40-125">Crée un formulaire Microsoft Office InfoPath basé sur le modèle de formulaire spécifié.</span><span class="sxs-lookup"><span data-stu-id="aeb40-125">Creates a new Microsoft Office InfoPath form based on the specified form template.</span></span>  <br/> |
|<span data-ttu-id="aeb40-126">**NewFromSolutionWithData** , méthode</span><span class="sxs-lookup"><span data-stu-id="aeb40-126">**NewFromSolutionWithData** method</span></span>  <br/> |<span data-ttu-id="aeb40-127">Crée un nouveau formulaire Microsoft Office InfoPath en utilisant le modèle de formulaire et les données XML spécifiés.</span><span class="sxs-lookup"><span data-stu-id="aeb40-127">Creates a new Microsoft Office InfoPath form using the specified XML data and form template.</span></span>  <br/> |
|<span data-ttu-id="aeb40-128">**Open** , méthode</span><span class="sxs-lookup"><span data-stu-id="aeb40-128">**Open** method</span></span>  <br/> |<span data-ttu-id="aeb40-129">Ouvre le formulaire Microsoft Office InfoPath spécifié.</span><span class="sxs-lookup"><span data-stu-id="aeb40-129">Opens the specified Microsoft Office InfoPath form.</span></span>  <br/> |
   
<span data-ttu-id="aeb40-130">Pour utiliser l'objet **application** à partir d'une application externe, utilisez la fonction **CreateObject** avec le ProgID de l'application InfoPath («InfoPath. application») pour créer une variable objet qui représente l'application InfoPath.</span><span class="sxs-lookup"><span data-stu-id="aeb40-130">To use the **Application** object from an external application, you use the **CreateObject** function with the ProgID of the InfoPath application ("InfoPath.Application") to create an object variable that represents the InfoPath application.</span></span> <span data-ttu-id="aeb40-131">Vous pouvez ensuite utiliser la propriété **XDocuments** pour accéder à la collection **XDocuments** et utiliser ses méthodes pour ouvrir ou créer un formulaire InfoPath.</span><span class="sxs-lookup"><span data-stu-id="aeb40-131">You can then use the **XDocuments** property to access the **XDocuments** collection and use its methods to open or create an InfoPath form.</span></span> <span data-ttu-id="aeb40-132">L'exemple suivant illustre la création d'une référence à l'objet **application** à l'aide du langage de programmation Microsoft visual Basic 6,0 ou Visual Basic pour applications (VBA):</span><span class="sxs-lookup"><span data-stu-id="aeb40-132">The following example demonstrates the creation of a reference to the **Application** object using the Microsoft Visual Basic 6.0 or Visual Basic for Applications (VBA) programming language:</span></span> 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> <span data-ttu-id="aeb40-133">Étant donné que la fonction **CreateObject** crée une variable d'objet à l'aide de la liaison tardive, la saisie semi-automatique des instructions n'est pas disponible dans Visual Basic Editor.</span><span class="sxs-lookup"><span data-stu-id="aeb40-133">Because the **CreateObject** function creates an object variable using late binding, automatic statement completion will not be available in the Visual Basic Editor.</span></span> <span data-ttu-id="aeb40-134">RePortez-vous aux liens dans les tableaux précédents pour obtenir des informations sur la syntaxe d'appel correcte.</span><span class="sxs-lookup"><span data-stu-id="aeb40-134">Refer to the links in the preceding tables for information about the correct calling syntax.</span></span> 
  

