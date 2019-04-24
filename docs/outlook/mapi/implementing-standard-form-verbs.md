---
title: Implémentation de verbes de formulaire standard
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6360b86dc23a5404b818f76cb1c2cd10747ef3cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317443"
---
# <a name="implementing-standard-form-verbs"></a><span data-ttu-id="4eb5f-103">Implémentation de verbes de formulaire standard</span><span class="sxs-lookup"><span data-stu-id="4eb5f-103">Implementing Standard Form Verbs</span></span>

  
  
<span data-ttu-id="4eb5f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4eb5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4eb5f-105">MAPI définit un ensemble de verbes standard, ou actions effectuées lorsqu'un utilisateur effectue une sélection de menu ou clique sur un bouton, que tous les visiteurs de formulaire doivent prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="4eb5f-105">MAPI defines a set of standard verbs, or actions taken when a user makes a menu selection or clicks a button, that all form viewers should support.</span></span> <span data-ttu-id="4eb5f-106">Chaque verbe a une constante associée à l'identification, définie dans le EXCHFORM. Fichier d'en-tête H.</span><span class="sxs-lookup"><span data-stu-id="4eb5f-106">Each verb has a constant associated with it for identification, defined in the EXCHFORM.H header file.</span></span> <span data-ttu-id="4eb5f-107">Le tableau suivant répertorie les verbes de formulaire standard et les constantes qui leur sont associées:</span><span class="sxs-lookup"><span data-stu-id="4eb5f-107">The following table lists the standard form verbs and their associated constants:</span></span>
  
|<span data-ttu-id="4eb5f-108">**Verb**</span><span class="sxs-lookup"><span data-stu-id="4eb5f-108">**Verb**</span></span>|<span data-ttu-id="4eb5f-109">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="4eb5f-109">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4eb5f-110">Ouvrir</span><span class="sxs-lookup"><span data-stu-id="4eb5f-110">Open</span></span>  <br/> |<span data-ttu-id="4eb5f-111">EXCHIVERB_OPEN</span><span class="sxs-lookup"><span data-stu-id="4eb5f-111">EXCHIVERB_OPEN</span></span>  <br/> |
|<span data-ttu-id="4eb5f-112">Répondre</span><span class="sxs-lookup"><span data-stu-id="4eb5f-112">Reply</span></span>  <br/> |<span data-ttu-id="4eb5f-113">EXCHIVERB_REPLYTOSENDER</span><span class="sxs-lookup"><span data-stu-id="4eb5f-113">EXCHIVERB_REPLYTOSENDER</span></span>  <br/> |
|<span data-ttu-id="4eb5f-114">Répondre à tous</span><span class="sxs-lookup"><span data-stu-id="4eb5f-114">Reply to All</span></span>  <br/> |<span data-ttu-id="4eb5f-115">EXCHIVERB_REPLYTOALL</span><span class="sxs-lookup"><span data-stu-id="4eb5f-115">EXCHIVERB_REPLYTOALL</span></span>  <br/> |
|<span data-ttu-id="4eb5f-116">Transférer</span><span class="sxs-lookup"><span data-stu-id="4eb5f-116">Forward</span></span>  <br/> |<span data-ttu-id="4eb5f-117">EXCHIVERB_FORWARD</span><span class="sxs-lookup"><span data-stu-id="4eb5f-117">EXCHIVERB_FORWARD</span></span>  <br/> |
|<span data-ttu-id="4eb5f-118">Print</span><span class="sxs-lookup"><span data-stu-id="4eb5f-118">Print</span></span>  <br/> |<span data-ttu-id="4eb5f-119">EXCHIVERB_PRINT</span><span class="sxs-lookup"><span data-stu-id="4eb5f-119">EXCHIVERB_PRINT</span></span>  <br/> |
|<span data-ttu-id="4eb5f-120">Enregistrer sous</span><span class="sxs-lookup"><span data-stu-id="4eb5f-120">Save As</span></span>  <br/> |<span data-ttu-id="4eb5f-121">EXCHIVERB_SAVEAS</span><span class="sxs-lookup"><span data-stu-id="4eb5f-121">EXCHIVERB_SAVEAS</span></span>  <br/> |
|<span data-ttu-id="4eb5f-122">Répondre dans le fichier</span><span class="sxs-lookup"><span data-stu-id="4eb5f-122">Reply to Folder</span></span>  <br/> |<span data-ttu-id="4eb5f-123">EXCHIVERB_REPLYTOFOLDER</span><span class="sxs-lookup"><span data-stu-id="4eb5f-123">EXCHIVERB_REPLYTOFOLDER</span></span>  <br/> |
   
<span data-ttu-id="4eb5f-124">Lorsqu'un utilisateur choisit un verbe, transmettez sa constante dans un appel à la méthode [IMAPIForm du formulaire::D overb](imapiform-doverb.md) pour effectuer l'action correspondante.</span><span class="sxs-lookup"><span data-stu-id="4eb5f-124">When a user chooses a verb, pass its constant in a call to the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method to perform its corresponding action.</span></span> 
  
<span data-ttu-id="4eb5f-125">Outre l'accès à des verbes via la visionneuse de formulaire, les utilisateurs peuvent parfois accéder à des verbes directement à partir du formulaire.</span><span class="sxs-lookup"><span data-stu-id="4eb5f-125">In addition to accessing verbs through your form viewer, users can sometimes access verbs directly from the form.</span></span> <span data-ttu-id="4eb5f-126">Par exemple, certains objets Form permettent à l'utilisateur d'appeler le verbe **Print** en cliquant avec le bouton droit sur le formulaire et en sélectionnant **Print** à partir d'un menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="4eb5f-126">For example, some form objects allow the user to invoke the **Print** verb by right-clicking on the form and choosing **Print** from a context-sensitive menu.</span></span> 
  

