---
title: Propriété canonique PidTagAttachExtension
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachExtension
api_type:
- HeaderDef
ms.assetid: 667da30b-e11c-4040-aecf-bb35eed23722
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 26efa868de29bc8a6a180b717230951b76da26a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319760"
---
# <a name="pidtagattachextension-canonical-property"></a><span data-ttu-id="7b7aa-103">Propriété canonique PidTagAttachExtension</span><span class="sxs-lookup"><span data-stu-id="7b7aa-103">PidTagAttachExtension Canonical Property</span></span>

  
  
<span data-ttu-id="7b7aa-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b7aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b7aa-105">Contient une extension de nom de fichier qui indique le type de document d’une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="7b7aa-105">Contains a file name extension that indicates the document type of an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b7aa-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="7b7aa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7b7aa-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span><span class="sxs-lookup"><span data-stu-id="7b7aa-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span></span>  <br/> |
|<span data-ttu-id="7b7aa-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="7b7aa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7b7aa-109">0x3703</span><span class="sxs-lookup"><span data-stu-id="7b7aa-109">0x3703</span></span>  <br/> |
|<span data-ttu-id="7b7aa-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="7b7aa-110">Data type:</span></span>  <br/> |<span data-ttu-id="7b7aa-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7b7aa-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7b7aa-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="7b7aa-112">Area:</span></span>  <br/> |<span data-ttu-id="7b7aa-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="7b7aa-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b7aa-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="7b7aa-114">Remarks</span></span>

<span data-ttu-id="7b7aa-115">Ces propriétés sont définies par l’application cliente au moment de la soumission.</span><span class="sxs-lookup"><span data-stu-id="7b7aa-115">These properties are set by the client application at submission time.</span></span> 
  
<span data-ttu-id="7b7aa-116">Le système de messagerie utilise **PR_ATTACH_EXTENSION** lors de la conversion de pièces jointes de messages (conversion sur route) ou du lancement d’applications basées sur des pièces jointes dans les messages reçus.</span><span class="sxs-lookup"><span data-stu-id="7b7aa-116">The messaging system uses **PR_ATTACH_EXTENSION** when converting message attachments (in-route conversion) or launching applications based on attachments in received messages.</span></span> <span data-ttu-id="7b7aa-117">Si le client d’envoi ne fournit pas de valeur pour ces propriétés, la boutique de messages qui gère la pièce jointe n’est pas tenue de la générer.</span><span class="sxs-lookup"><span data-stu-id="7b7aa-117">If the sending client does not provide a value for these properties, the message store handling the attachment is not obligated to generate it.</span></span> <span data-ttu-id="7b7aa-118">Le client de réception doit d’abord vérifier la PR_ATTACH_EXTENSION et, si elle n’est pas fournie, doit l’parer à partir de la propriété **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) ou **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="7b7aa-118">The receiving client should first check for **PR_ATTACH_EXTENSION**, and if it is not provided, should parse the file name extension from the attachment's **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) or **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7b7aa-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="7b7aa-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7b7aa-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="7b7aa-120">Protocol specifications</span></span>

<span data-ttu-id="7b7aa-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b7aa-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b7aa-122">Gère les objets message et pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="7b7aa-122">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7b7aa-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="7b7aa-123">Header files</span></span>

<span data-ttu-id="7b7aa-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7b7aa-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="7b7aa-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="7b7aa-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="7b7aa-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7b7aa-126">Mapitags.h</span></span>
  
> <span data-ttu-id="7b7aa-127">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="7b7aa-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b7aa-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b7aa-128">See also</span></span>



[<span data-ttu-id="7b7aa-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="7b7aa-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7b7aa-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="7b7aa-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7b7aa-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="7b7aa-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7b7aa-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="7b7aa-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

