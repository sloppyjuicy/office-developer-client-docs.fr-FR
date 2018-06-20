---
title: Implémentation de verbes formulaire Standard
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8135af7947f30ac600b8d9af364b2a79a3443ab6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784200"
---
# <a name="implementing-standard-form-verbs"></a><span data-ttu-id="87316-103">Implémentation de verbes formulaire Standard</span><span class="sxs-lookup"><span data-stu-id="87316-103">Implementing Standard Form Verbs</span></span>

  
  
<span data-ttu-id="87316-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="87316-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="87316-105">MAPI définit un ensemble de verbes standard ou les actions effectuées lorsqu’un utilisateur effectue une sélection de menu ou clique sur un bouton, toutes les visionneuses de formulaire doivent prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="87316-105">MAPI defines a set of standard verbs, or actions taken when a user makes a menu selection or clicks a button, that all form viewers should support.</span></span> <span data-ttu-id="87316-106">Chaque verbe possède une constante associée à l’identification, définie dans le EXCHFORM. Fichier d’en-tête H.</span><span class="sxs-lookup"><span data-stu-id="87316-106">Each verb has a constant associated with it for identification, defined in the EXCHFORM.H header file.</span></span> <span data-ttu-id="87316-107">Le tableau suivant répertorie les verbes formulaire standard et les constantes associées :</span><span class="sxs-lookup"><span data-stu-id="87316-107">The following table lists the standard form verbs and their associated constants:</span></span>
  
|<span data-ttu-id="87316-108">**Verbe**</span><span class="sxs-lookup"><span data-stu-id="87316-108">**Verb**</span></span>|<span data-ttu-id="87316-109">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="87316-109">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="87316-110">Ouvrir</span><span class="sxs-lookup"><span data-stu-id="87316-110">Open</span></span>  <br/> |<span data-ttu-id="87316-111">EXCHIVERB_OPEN</span><span class="sxs-lookup"><span data-stu-id="87316-111">EXCHIVERB_OPEN</span></span>  <br/> |
|<span data-ttu-id="87316-112">Répondre</span><span class="sxs-lookup"><span data-stu-id="87316-112">Reply</span></span>  <br/> |<span data-ttu-id="87316-113">EXCHIVERB_REPLYTOSENDER</span><span class="sxs-lookup"><span data-stu-id="87316-113">EXCHIVERB_REPLYTOSENDER</span></span>  <br/> |
|<span data-ttu-id="87316-114">Répondre à tous</span><span class="sxs-lookup"><span data-stu-id="87316-114">Reply to All</span></span>  <br/> |<span data-ttu-id="87316-115">EXCHIVERB_REPLYTOALL</span><span class="sxs-lookup"><span data-stu-id="87316-115">EXCHIVERB_REPLYTOALL</span></span>  <br/> |
|<span data-ttu-id="87316-116">Transférer</span><span class="sxs-lookup"><span data-stu-id="87316-116">Forward</span></span>  <br/> |<span data-ttu-id="87316-117">EXCHIVERB_FORWARD</span><span class="sxs-lookup"><span data-stu-id="87316-117">EXCHIVERB_FORWARD</span></span>  <br/> |
|<span data-ttu-id="87316-118">Imprimer</span><span class="sxs-lookup"><span data-stu-id="87316-118">Print</span></span>  <br/> |<span data-ttu-id="87316-119">EXCHIVERB_PRINT</span><span class="sxs-lookup"><span data-stu-id="87316-119">EXCHIVERB_PRINT</span></span>  <br/> |
|<span data-ttu-id="87316-120">Enregistrer en tant que</span><span class="sxs-lookup"><span data-stu-id="87316-120">Save As</span></span>  <br/> |<span data-ttu-id="87316-121">EXCHIVERB_SAVEAS</span><span class="sxs-lookup"><span data-stu-id="87316-121">EXCHIVERB_SAVEAS</span></span>  <br/> |
|<span data-ttu-id="87316-122">Répondre à un dossier</span><span class="sxs-lookup"><span data-stu-id="87316-122">Reply to Folder</span></span>  <br/> |<span data-ttu-id="87316-123">EXCHIVERB_REPLYTOFOLDER</span><span class="sxs-lookup"><span data-stu-id="87316-123">EXCHIVERB_REPLYTOFOLDER</span></span>  <br/> |
   
<span data-ttu-id="87316-124">Lorsqu’un utilisateur choisit un verbe, transmettez la constante dans un appel à la méthode du formulaire [IMAPIForm::DoVerb](imapiform-doverb.md) pour effectuer son action correspondante.</span><span class="sxs-lookup"><span data-stu-id="87316-124">When a user chooses a verb, pass its constant in a call to the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method to perform its corresponding action.</span></span> 
  
<span data-ttu-id="87316-125">En plus de l’accès à des verbes via votre visionneuse de formulaire, les utilisateurs peuvent accéder parfois verbes directement à partir du formulaire.</span><span class="sxs-lookup"><span data-stu-id="87316-125">In addition to accessing verbs through your form viewer, users can sometimes access verbs directly from the form.</span></span> <span data-ttu-id="87316-126">Par exemple, certains objets formulaire autorise l’utilisateur à appeler le verbe **Imprimer** en avec le bouton droit sur le formulaire et en choisissant **Imprimer** dans un menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="87316-126">For example, some form objects allow the user to invoke the **Print** verb by right-clicking on the form and choosing **Print** from a context-sensitive menu.</span></span> 
  

