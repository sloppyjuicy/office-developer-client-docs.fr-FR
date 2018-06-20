---
title: Propriété canonique PidTagDisplayTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTo
api_type:
- HeaderDef
ms.assetid: 700cc03b-5d98-40ce-adb5-a11fdac8aa28
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d83683fded6a650a947caa7119d138f6f4105e1b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785952"
---
# <a name="pidtagdisplayto-canonical-property"></a><span data-ttu-id="eb03a-103">Propriété canonique PidTagDisplayTo</span><span class="sxs-lookup"><span data-stu-id="eb03a-103">PidTagDisplayTo Canonical Property</span></span>

  
  
<span data-ttu-id="eb03a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eb03a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eb03a-105">Contient une liste des noms complets du principal (à) destinataires du message, séparés par des points-virgules ( ;).</span><span class="sxs-lookup"><span data-stu-id="eb03a-105">Contains a list of the display names of the primary (To) message recipients, separated by semicolons (;).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eb03a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="eb03a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eb03a-107">PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W</span><span class="sxs-lookup"><span data-stu-id="eb03a-107">PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W</span></span>  <br/> |
|<span data-ttu-id="eb03a-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="eb03a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="eb03a-109">0x0E04</span><span class="sxs-lookup"><span data-stu-id="eb03a-109">0x0E04</span></span>  <br/> |
|<span data-ttu-id="eb03a-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="eb03a-110">Data type:</span></span>  <br/> |<span data-ttu-id="eb03a-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="eb03a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="eb03a-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="eb03a-112">Area:</span></span>  <br/> |<span data-ttu-id="eb03a-113">Message</span><span class="sxs-lookup"><span data-stu-id="eb03a-113">Message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb03a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="eb03a-114">Remarks</span></span>

<span data-ttu-id="eb03a-115">La banque de messages calcule ces propriétés sur les objets de message à l’aide de la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="eb03a-115">The message store computes these properties on message objects by using the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="eb03a-116">La banque de messages gère également ces propriétés pour qu’elle reflète toujours le dernier état enregistré d’un message.</span><span class="sxs-lookup"><span data-stu-id="eb03a-116">The message store also maintains these properties so that it always reflects the last saved state of a message.</span></span> <span data-ttu-id="eb03a-117">La valeur est synchronisée au moment de chaque appel à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="eb03a-117">The value is synchronized at the time of every call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="eb03a-118">Si un message n’a pas de destinataire principales, la banque de messages doit répondre à un appel de [IMAPIProp::GetProps](imapiprop-getprops.md) avec une valeur de retour de S_OK et une chaîne vide pour **PR_DISPLAY_TO**.</span><span class="sxs-lookup"><span data-stu-id="eb03a-118">If a message has no primary recipients, the message store should respond to an [IMAPIProp::GetProps](imapiprop-getprops.md) call with a return value of S_OK and an empty string for **PR_DISPLAY_TO**.</span></span> 
  
<span data-ttu-id="eb03a-119">En raison de la nécessité de possible pour la localisation, MAPI fournit ces instructions pour tous les noms des destinataires :</span><span class="sxs-lookup"><span data-stu-id="eb03a-119">Because of the possible need for localization, MAPI provides these guidelines for all recipient names:</span></span>
  
- <span data-ttu-id="eb03a-120">Les noms doivent être en mesure d’être localisés.</span><span class="sxs-lookup"><span data-stu-id="eb03a-120">All names should be able to be localized.</span></span> 
    
- <span data-ttu-id="eb03a-121">Le point-virgule doit être le caractère utilisé pour séparer les noms dans les propriétés **PR_DISPLAY_TO** , **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) et **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="eb03a-121">The semicolon should be the character that is used to separate names in the **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)), and **PR_DISPLAY_TO** properties.</span></span> <span data-ttu-id="eb03a-122">Des points-virgules ne sont pas autorisés dans les noms de destinataires dans MAPI.</span><span class="sxs-lookup"><span data-stu-id="eb03a-122">Semicolons are not permitted within recipient names in MAPI.</span></span> 
    
- <span data-ttu-id="eb03a-123">Les clients doivent traduire chaque point-virgule rencontré **PR_DISPLAY_TO** les propriétés associées à un caractère de séparation localisés avant de rendre les informations visibles dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eb03a-123">Clients should translate each semicolon encountered in the **PR_DISPLAY_TO** and related properties to a localized separator character before making the information visible in the user interface.</span></span> 
    
- <span data-ttu-id="eb03a-124">Lors du transfert des messages, les clients est inutile de traduire les caractères de séparation de la ligne de destinataire principale.</span><span class="sxs-lookup"><span data-stu-id="eb03a-124">When forwarding messages, clients do not need to translate the separator characters on the primary recipient line.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="eb03a-125">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="eb03a-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="eb03a-126">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="eb03a-126">Protocol specifications</span></span>

<span data-ttu-id="eb03a-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb03a-127">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eb03a-128">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="eb03a-128">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="eb03a-129">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="eb03a-129">Header files</span></span>

<span data-ttu-id="eb03a-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eb03a-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="eb03a-131">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="eb03a-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="eb03a-132">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="eb03a-132">Mapitags.h</span></span>
  
> <span data-ttu-id="eb03a-133">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="eb03a-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eb03a-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb03a-134">See also</span></span>



[<span data-ttu-id="eb03a-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="eb03a-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eb03a-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="eb03a-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eb03a-137">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="eb03a-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eb03a-138">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="eb03a-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

