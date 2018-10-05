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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387747"
---
# <a name="pidtagsearchrecipientemailbcc-canonical-property"></a><span data-ttu-id="2ea27-103">Propriété canonique PidTagSearchRecipientEmailBcc</span><span class="sxs-lookup"><span data-stu-id="2ea27-103">PidTagSearchRecipientEmailBcc Canonical Property</span></span>

  
  
<span data-ttu-id="2ea27-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ea27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ea27-105">Contient une chaîne Unicode qui est interrogée dans la liste des adresses de messagerie ou les noms complets des destinataires dans la ligne **Cci** des messages en attente sur le magasin.</span><span class="sxs-lookup"><span data-stu-id="2ea27-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients addressed in the **BCC** line of unsent messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="2ea27-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="2ea27-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ea27-107">PR_SEARCH_RECIP_EMAIL_BCC_W</span><span class="sxs-lookup"><span data-stu-id="2ea27-107">PR_SEARCH_RECIP_EMAIL_BCC_W</span></span>  <br/> |
|<span data-ttu-id="2ea27-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="2ea27-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2ea27-109">0x0EA8</span><span class="sxs-lookup"><span data-stu-id="2ea27-109">0x0EA8</span></span>  <br/> |
|<span data-ttu-id="2ea27-110">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="2ea27-110">Property type:</span></span>  <br/> |<span data-ttu-id="2ea27-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2ea27-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2ea27-112">Access :</span><span class="sxs-lookup"><span data-stu-id="2ea27-112">Access:</span></span>  <br/> |<span data-ttu-id="2ea27-113">Recherche</span><span class="sxs-lookup"><span data-stu-id="2ea27-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ea27-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="2ea27-114">Remarks</span></span>

<span data-ttu-id="2ea27-115">Cette propriété est uniquement aux messages qui n’ont pas été envoyés, dans le magasin étant donné que les messages qui ont été envoyés ou reçus ne contiennent pas d’informations Cci.</span><span class="sxs-lookup"><span data-stu-id="2ea27-115">This property is only relevant to messages on the store that have not been sent, because messages that have been sent or received do not contain BCC information.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2ea27-116">Cette balise de restriction MAPI, utilisée pour rechercher des adresses de messagerie ou des noms d’affichage vers lequel le message sera envoyé en tant que copie carbone invisible, pas peut-être être définie dans le fichier d’en-tête téléchargeable dont vous disposez.</span><span class="sxs-lookup"><span data-stu-id="2ea27-116">This MAPI restriction tag, used when searching for email addresses or display names to which the message will be sent as a blind carbon copy, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="2ea27-117">Vous pouvez l’ajouter à votre code à l’aide de la valeur suivante : >`#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`</span><span class="sxs-lookup"><span data-stu-id="2ea27-117">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2ea27-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="2ea27-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2ea27-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="2ea27-119">Protocol specifications</span></span>

<span data-ttu-id="2ea27-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ea27-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ea27-121">Fournit des références aux spécifications du protocole connexes Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2ea27-121">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2ea27-122">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ea27-122">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ea27-123">Spécifie les propriétés et opérations pour la manipulation d’une configuration de liste de dossier de recherche.</span><span class="sxs-lookup"><span data-stu-id="2ea27-123">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2ea27-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="2ea27-124">Header files</span></span>

<span data-ttu-id="2ea27-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ea27-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ea27-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="2ea27-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="2ea27-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="2ea27-127">Mapitags.h</span></span>
  
> <span data-ttu-id="2ea27-128">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="2ea27-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ea27-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ea27-129">See also</span></span>



[<span data-ttu-id="2ea27-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="2ea27-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ea27-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="2ea27-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ea27-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="2ea27-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ea27-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="2ea27-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

