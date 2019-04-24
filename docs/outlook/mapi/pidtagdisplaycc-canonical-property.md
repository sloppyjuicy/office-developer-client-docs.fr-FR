---
title: Propriété canonique PidTagDisplayCc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayCc
api_type:
- HeaderDef
ms.assetid: 00377e78-a208-4942-a7a6-893b2a71ab0b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2bf862317ca1d2f2a09a71e1af62b82661b33326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360808"
---
# <a name="pidtagdisplaycc-canonical-property"></a><span data-ttu-id="6ff20-103">Propriété canonique PidTagDisplayCc</span><span class="sxs-lookup"><span data-stu-id="6ff20-103">PidTagDisplayCc Canonical Property</span></span>

  
  
<span data-ttu-id="6ff20-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ff20-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ff20-105">Contient une liste ASCII des noms d'affichage des destinataires de messages CC (copie carbone), séparés par des points-virgules (;).</span><span class="sxs-lookup"><span data-stu-id="6ff20-105">Contains an ASCII list of the display names of any carbon copy (CC) message recipients, separated by semicolons (;).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6ff20-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6ff20-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6ff20-107">PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W</span><span class="sxs-lookup"><span data-stu-id="6ff20-107">PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W</span></span>  <br/> |
|<span data-ttu-id="6ff20-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6ff20-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6ff20-109">0x0E03</span><span class="sxs-lookup"><span data-stu-id="6ff20-109">0x0E03</span></span>  <br/> |
|<span data-ttu-id="6ff20-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6ff20-110">Data type:</span></span>  <br/> |<span data-ttu-id="6ff20-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6ff20-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6ff20-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="6ff20-112">Area:</span></span>  <br/> |<span data-ttu-id="6ff20-113">Message</span><span class="sxs-lookup"><span data-stu-id="6ff20-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ff20-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6ff20-114">Remarks</span></span>

<span data-ttu-id="6ff20-115">La Banque de messages calcule ces propriétés sur les objets de message à l'aide de la méthode [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="6ff20-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="6ff20-116">La Banque de messages gère également ces propriétés de sorte qu'elle reflète toujours le dernier état enregistré d'un message.</span><span class="sxs-lookup"><span data-stu-id="6ff20-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="6ff20-117">La valeur est synchronisée au moment de chaque appel à [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="6ff20-117">The value is synchronized at the time of every call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> 
  
<span data-ttu-id="6ff20-118">Si un message n'a pas de destinataires en copie carbone, la Banque de messages doit répondre à un appel [IMAPIProp:: GetProps](imapiprop-getprops.md) avec une valeur de retour de S_OK et une chaîne vide pour ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6ff20-118">If a message has no carbon copy recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for these properties.</span></span> 
  
<span data-ttu-id="6ff20-119">En raison de l'éventuel besoin de localisation, MAPI fournit les instructions suivantes pour tous les noms de destinataires:</span><span class="sxs-lookup"><span data-stu-id="6ff20-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="6ff20-120">Tous les noms doivent pouvoir être localisés.</span><span class="sxs-lookup"><span data-stu-id="6ff20-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="6ff20-121">Le point-virgule doit être le caractère utilisé pour séparer les noms dans les propriétés **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC**et **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6ff20-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC**, and **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) properties.</span></span> <span data-ttu-id="6ff20-122">Les points-virgules ne sont pas autorisés dans les noms de destinataires dans MAPI.</span><span class="sxs-lookup"><span data-stu-id="6ff20-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="6ff20-123">Les clients doivent traduire chaque point-virgule rencontré dans cette propriété en un caractère de séparation localisé avant de rendre les informations de propriété visibles dans l'interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6ff20-123">Clients should translate each semicolon encountered in this property to a localized separator character before making the property information visible in the user interface.</span></span> 
    
- <span data-ttu-id="6ff20-124">Lors du transfert de messages, les clients n'ont pas besoin de traduire les caractères de séparation sur la ligne du destinataire de la copie carbone.</span><span class="sxs-lookup"><span data-stu-id="6ff20-124">When forwarding messages, clients do not need to translate the separator characters on the carbon copy recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="6ff20-125">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="6ff20-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6ff20-126">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="6ff20-126">Protocol specifications</span></span>

<span data-ttu-id="6ff20-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ff20-127">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ff20-128">Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.</span><span class="sxs-lookup"><span data-stu-id="6ff20-128">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6ff20-129">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="6ff20-129">Header files</span></span>

<span data-ttu-id="6ff20-130">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6ff20-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="6ff20-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6ff20-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="6ff20-132">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="6ff20-132">Mapitags.h</span></span>
  
> <span data-ttu-id="6ff20-133">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="6ff20-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6ff20-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ff20-134">See also</span></span>



[<span data-ttu-id="6ff20-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6ff20-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6ff20-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6ff20-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6ff20-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6ff20-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6ff20-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="6ff20-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

