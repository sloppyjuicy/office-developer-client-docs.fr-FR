---
title: Propriété canonique PidTagJunkIncludeContacts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkIncludeContacts
api_type:
- HeaderDef
ms.assetid: 25368f6c-4fba-4381-840c-ca122bd31b5f
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 121bba82a9ccd40a435769b5eb2d966ed60575f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586969"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a><span data-ttu-id="695b3-103">Propriété canonique PidTagJunkIncludeContacts</span><span class="sxs-lookup"><span data-stu-id="695b3-103">PidTagJunkIncludeContacts Canonical Property</span></span>

  
  
<span data-ttu-id="695b3-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="695b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="695b3-105">Indique si les adresses de messagerie des contacts du dossier Contacts sont traités spécialement en ce qui concerne le filtre de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="695b3-105">Indicates whether email addresses of the contacts in the Contacts folder are treated specially with respect to the spam filter.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="695b3-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="695b3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="695b3-107">PR_JUNK_INCLUDE_CONTACTS</span><span class="sxs-lookup"><span data-stu-id="695b3-107">PR_JUNK_INCLUDE_CONTACTS</span></span>  <br/> |
|<span data-ttu-id="695b3-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="695b3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="695b3-109">0x6100</span><span class="sxs-lookup"><span data-stu-id="695b3-109">0x6100</span></span>  <br/> |
|<span data-ttu-id="695b3-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="695b3-110">Data type:</span></span>  <br/> |<span data-ttu-id="695b3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="695b3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="695b3-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="695b3-112">Area:</span></span>  <br/> |<span data-ttu-id="695b3-113">Courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="695b3-113">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="695b3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="695b3-114">Remarks</span></span>

<span data-ttu-id="695b3-115">Si la valeur « 0 x 00000001 », ces adresses de messagerie doivent remplir la partie de la Restriction de règle de courrier indésirable adresse de messagerie du contact « approuvés » tels que le courrier provenant de ces adresses est considéré comme « pas de courrier indésirable ».</span><span class="sxs-lookup"><span data-stu-id="695b3-115">If set to "0x00000001", these email addresses must populate the "trusted" contact email address portion of the Junk E-Mail Rule Restriction such that mail from these addresses is treated as "not junk".</span></span> <span data-ttu-id="695b3-116">Si la valeur « 0 x 00000000 », les adresses de messagerie à partir du dossier Contacts ne doivent pas être ajoutés à la règle de courrier indésirable et la section de la règle doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="695b3-116">If set to "0x00000000", email addresses from the Contacts folder must not be added to the Junk E-Mail Rule, and the section of the rule must be NULL.</span></span>
  
<span data-ttu-id="695b3-117">Si cette propriété est présente avec la valeur « 0 x 00000001 » et si le contact ajouté les adresses de messagerie qui ne sont pas encore inclus dans la section contacts approuvé de la règle de courrier indésirable, les adresses de messagerie doivent être ajoutés à la restriction.</span><span class="sxs-lookup"><span data-stu-id="695b3-117">If this property is present with a value of "0x00000001" and if the added contact has email addresses that are not yet included in the trusted contacts section of the Junk E-Mail Rule, those email addresses must be added to the restriction.</span></span> <span data-ttu-id="695b3-118">Si cette propriété est « 0 x 00000000 », aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="695b3-118">If this property is "0x00000000", no action is required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="695b3-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="695b3-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="695b3-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="695b3-120">Protocol specifications</span></span>

<span data-ttu-id="695b3-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="695b3-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="695b3-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="695b3-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="695b3-123">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="695b3-123">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="695b3-124">Permet la gestion des listes autoriser/bloquer et la détermination des messages de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="695b3-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="695b3-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="695b3-125">Header files</span></span>

<span data-ttu-id="695b3-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="695b3-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="695b3-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="695b3-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="695b3-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="695b3-128">Mapitags.h</span></span>
  
> <span data-ttu-id="695b3-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="695b3-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="695b3-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="695b3-130">See also</span></span>



[<span data-ttu-id="695b3-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="695b3-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="695b3-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="695b3-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="695b3-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="695b3-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="695b3-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="695b3-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

