---
title: Propriété canonique PidTagSearchRecipientEmailBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d9561d13-8d52-500c-5369-15a2cf5c92c3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5b0db4b3bc7903aae74fa7275d3e27e22d628514
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359156"
---
# <a name="pidtagsearchrecipientemailbcc-canonical-property"></a><span data-ttu-id="f7ad6-103">Propriété canonique PidTagSearchRecipientEmailBcc</span><span class="sxs-lookup"><span data-stu-id="f7ad6-103">PidTagSearchRecipientEmailBcc Canonical Property</span></span>

  
  
<span data-ttu-id="f7ad6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7ad6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7ad6-105">Contient une chaîne Unicode en cours d’interrogation dans la liste des adresses de messagerie ou affiche les noms des destinataires adressés dans la ligne **BcC** des messages non envoyés dans la banque.</span><span class="sxs-lookup"><span data-stu-id="f7ad6-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients addressed in the **BCC** line of unsent messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="f7ad6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f7ad6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f7ad6-107">PR_SEARCH_RECIP_EMAIL_BCC_W</span><span class="sxs-lookup"><span data-stu-id="f7ad6-107">PR_SEARCH_RECIP_EMAIL_BCC_W</span></span>  <br/> |
|<span data-ttu-id="f7ad6-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f7ad6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f7ad6-109">0x0EA8</span><span class="sxs-lookup"><span data-stu-id="f7ad6-109">0x0EA8</span></span>  <br/> |
|<span data-ttu-id="f7ad6-110">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="f7ad6-110">Property type:</span></span>  <br/> |<span data-ttu-id="f7ad6-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f7ad6-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f7ad6-112">Accès :</span><span class="sxs-lookup"><span data-stu-id="f7ad6-112">Access:</span></span>  <br/> |<span data-ttu-id="f7ad6-113">Recherche</span><span class="sxs-lookup"><span data-stu-id="f7ad6-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7ad6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f7ad6-114">Remarks</span></span>

<span data-ttu-id="f7ad6-115">Cette propriété est uniquement pertinente pour les messages de la boutique qui n’ont pas été envoyés, car les messages qui ont été envoyés ou reçus ne contiennent pas d’informations bcc.</span><span class="sxs-lookup"><span data-stu-id="f7ad6-115">This property is only relevant to messages on the store that have not been sent, because messages that have been sent or received do not contain BCC information.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f7ad6-116">Cette balise de restriction MAPI, utilisée lors de la recherche d’adresses de messagerie ou de noms complets vers lesquels le message sera envoyé en tant que copie carbone non voyante, peut ne pas être définie dans le fichier d’en-tête téléchargeable dont vous disposez actuellement.</span><span class="sxs-lookup"><span data-stu-id="f7ad6-116">This MAPI restriction tag, used when searching for email addresses or display names to which the message will be sent as a blind carbon copy, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="f7ad6-117">Vous pouvez l’ajouter à votre code en utilisant la valeur suivante : >  `#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`</span><span class="sxs-lookup"><span data-stu-id="f7ad6-117">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f7ad6-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f7ad6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f7ad6-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="f7ad6-119">Protocol specifications</span></span>

<span data-ttu-id="f7ad6-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7ad6-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7ad6-121">Fournit des références aux spécifications Microsoft Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="f7ad6-121">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f7ad6-122">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7ad6-122">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7ad6-123">Spécifie les propriétés et opérations de manipulation d’une configuration de liste de dossiers de recherche.</span><span class="sxs-lookup"><span data-stu-id="f7ad6-123">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f7ad6-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f7ad6-124">Header files</span></span>

<span data-ttu-id="f7ad6-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f7ad6-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f7ad6-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f7ad6-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="f7ad6-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f7ad6-127">Mapitags.h</span></span>
  
> <span data-ttu-id="f7ad6-128">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="f7ad6-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f7ad6-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7ad6-129">See also</span></span>



[<span data-ttu-id="f7ad6-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f7ad6-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f7ad6-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f7ad6-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f7ad6-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f7ad6-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f7ad6-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f7ad6-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

