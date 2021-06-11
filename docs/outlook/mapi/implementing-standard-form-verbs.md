---
title: Mise en œuvre de verbes de formulaire standard
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6360b86dc23a5404b818f76cb1c2cd10747ef3cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426120"
---
# <a name="implementing-standard-form-verbs"></a><span data-ttu-id="604fe-103">Mise en œuvre de verbes de formulaire standard</span><span class="sxs-lookup"><span data-stu-id="604fe-103">Implementing Standard Form Verbs</span></span>

  
  
<span data-ttu-id="604fe-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="604fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="604fe-105">MAPI définit un ensemble de verbes standard, ou actions entreprises lorsqu’un utilisateur effectue une sélection de menu ou clique sur un bouton, que toutes les visionneuses de formulaire doivent prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="604fe-105">MAPI defines a set of standard verbs, or actions taken when a user makes a menu selection or clicks a button, that all form viewers should support.</span></span> <span data-ttu-id="604fe-106">Chaque verbe est associé à une constante pour l’identification, définie dans l’EXCHFORM. Fichier d’en-tête H.</span><span class="sxs-lookup"><span data-stu-id="604fe-106">Each verb has a constant associated with it for identification, defined in the EXCHFORM.H header file.</span></span> <span data-ttu-id="604fe-107">Le tableau suivant répertorie les verbes de formulaire standard et leurs constantes associées :</span><span class="sxs-lookup"><span data-stu-id="604fe-107">The following table lists the standard form verbs and their associated constants:</span></span>
  
|<span data-ttu-id="604fe-108">**Verb**</span><span class="sxs-lookup"><span data-stu-id="604fe-108">**Verb**</span></span>|<span data-ttu-id="604fe-109">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="604fe-109">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="604fe-110">Ouvrir</span><span class="sxs-lookup"><span data-stu-id="604fe-110">Open</span></span>  <br/> |<span data-ttu-id="604fe-111">EXCHIVERB_OPEN</span><span class="sxs-lookup"><span data-stu-id="604fe-111">EXCHIVERB_OPEN</span></span>  <br/> |
|<span data-ttu-id="604fe-112">Répondre</span><span class="sxs-lookup"><span data-stu-id="604fe-112">Reply</span></span>  <br/> |<span data-ttu-id="604fe-113">EXCHIVERB_REPLYTOSENDER</span><span class="sxs-lookup"><span data-stu-id="604fe-113">EXCHIVERB_REPLYTOSENDER</span></span>  <br/> |
|<span data-ttu-id="604fe-114">Répondre à tous</span><span class="sxs-lookup"><span data-stu-id="604fe-114">Reply to All</span></span>  <br/> |<span data-ttu-id="604fe-115">EXCHIVERB_REPLYTOALL</span><span class="sxs-lookup"><span data-stu-id="604fe-115">EXCHIVERB_REPLYTOALL</span></span>  <br/> |
|<span data-ttu-id="604fe-116">Transférer</span><span class="sxs-lookup"><span data-stu-id="604fe-116">Forward</span></span>  <br/> |<span data-ttu-id="604fe-117">EXCHIVERB_FORWARD</span><span class="sxs-lookup"><span data-stu-id="604fe-117">EXCHIVERB_FORWARD</span></span>  <br/> |
|<span data-ttu-id="604fe-118">Imprimer</span><span class="sxs-lookup"><span data-stu-id="604fe-118">Print</span></span>  <br/> |<span data-ttu-id="604fe-119">EXCHIVERB_PRINT</span><span class="sxs-lookup"><span data-stu-id="604fe-119">EXCHIVERB_PRINT</span></span>  <br/> |
|<span data-ttu-id="604fe-120">Enregistrer sous</span><span class="sxs-lookup"><span data-stu-id="604fe-120">Save As</span></span>  <br/> |<span data-ttu-id="604fe-121">EXCHIVERB_SAVEAS</span><span class="sxs-lookup"><span data-stu-id="604fe-121">EXCHIVERB_SAVEAS</span></span>  <br/> |
|<span data-ttu-id="604fe-122">Répondre dans le fichier</span><span class="sxs-lookup"><span data-stu-id="604fe-122">Reply to Folder</span></span>  <br/> |<span data-ttu-id="604fe-123">EXCHIVERB_REPLYTOFOLDER</span><span class="sxs-lookup"><span data-stu-id="604fe-123">EXCHIVERB_REPLYTOFOLDER</span></span>  <br/> |
   
<span data-ttu-id="604fe-124">Lorsqu’un utilisateur choisit un verbe, passez sa constante dans un appel à la méthode [IMAPIForm::D oVerb](imapiform-doverb.md) du formulaire pour effectuer son action correspondante.</span><span class="sxs-lookup"><span data-stu-id="604fe-124">When a user chooses a verb, pass its constant in a call to the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method to perform its corresponding action.</span></span> 
  
<span data-ttu-id="604fe-125">En plus d’accéder aux verbes via votre visionneuse de formulaires, les utilisateurs peuvent parfois accéder aux verbes directement à partir du formulaire.</span><span class="sxs-lookup"><span data-stu-id="604fe-125">In addition to accessing verbs through your form viewer, users can sometimes access verbs directly from the form.</span></span> <span data-ttu-id="604fe-126">Par exemple, certains objets de formulaire  permettent à l’utilisateur d’appeler le  verbe Imprimer en cliquant avec le bouton droit sur le formulaire et en choisissant Imprimer à partir d’un menu contextuelle.</span><span class="sxs-lookup"><span data-stu-id="604fe-126">For example, some form objects allow the user to invoke the **Print** verb by right-clicking on the form and choosing **Print** from a context-sensitive menu.</span></span> 
  

