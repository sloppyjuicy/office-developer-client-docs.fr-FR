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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4d71a0e26e2043bbaf961ae5096afc5789be36be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785720"
---
# <a name="pidtagattachextension-canonical-property"></a><span data-ttu-id="026ad-103">Propriété canonique PidTagAttachExtension</span><span class="sxs-lookup"><span data-stu-id="026ad-103">PidTagAttachExtension Canonical Property</span></span>

  
  
<span data-ttu-id="026ad-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="026ad-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="026ad-105">Contient une extension de nom de fichier qui indique le type de document d’une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="026ad-105">Contains a file name extension that indicates the document type of an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="026ad-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="026ad-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="026ad-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span><span class="sxs-lookup"><span data-stu-id="026ad-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span></span>  <br/> |
|<span data-ttu-id="026ad-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="026ad-108">Identifier:</span></span>  <br/> |<span data-ttu-id="026ad-109">0x3703</span><span class="sxs-lookup"><span data-stu-id="026ad-109">0x3703</span></span>  <br/> |
|<span data-ttu-id="026ad-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="026ad-110">Data type:</span></span>  <br/> |<span data-ttu-id="026ad-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="026ad-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="026ad-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="026ad-112">Area:</span></span>  <br/> |<span data-ttu-id="026ad-113">Pièce jointe du message</span><span class="sxs-lookup"><span data-stu-id="026ad-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="026ad-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="026ad-114">Remarks</span></span>

<span data-ttu-id="026ad-115">Ces propriétés sont définies par l’application cliente au moment de l’envoi.</span><span class="sxs-lookup"><span data-stu-id="026ad-115">These properties are set by the client application at submission time.</span></span> 
  
<span data-ttu-id="026ad-116">Le système utilise **PR_ATTACH_EXTENSION** de messagerie lors de la conversion des pièces jointes des messages (conversion dans itinéraire) ou lancer des applications basées sur les pièces jointes dans les messages reçus.</span><span class="sxs-lookup"><span data-stu-id="026ad-116">The messaging system uses **PR_ATTACH_EXTENSION** when converting message attachments (in-route conversion) or launching applications based on attachments in received messages.</span></span> <span data-ttu-id="026ad-117">Si le client d’envoi ne fournit pas une valeur pour ces propriétés, la banque de messages gère la pièce jointe n’est pas obligée de générer.</span><span class="sxs-lookup"><span data-stu-id="026ad-117">If the sending client does not provide a value for these properties, the message store handling the attachment is not obligated to generate it.</span></span> <span data-ttu-id="026ad-118">Le client destinataire doit d’abord vérifier **PR_ATTACH_EXTENSION**et si elle n’est pas fourni, doit analyser l’extension de nom de fichier à partir de la pièce jointe **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) ou **PR_ATTACH_LONG_FILENAME **Propriété ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="026ad-118">The receiving client should first check for **PR_ATTACH_EXTENSION**, and if it is not provided, should parse the file name extension from the attachment's **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) or **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="026ad-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="026ad-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="026ad-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="026ad-120">Protocol specifications</span></span>

<span data-ttu-id="026ad-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="026ad-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="026ad-122">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="026ad-122">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="026ad-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="026ad-123">Header files</span></span>

<span data-ttu-id="026ad-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="026ad-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="026ad-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="026ad-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="026ad-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="026ad-126">Mapitags.h</span></span>
  
> <span data-ttu-id="026ad-127">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="026ad-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="026ad-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="026ad-128">See also</span></span>



[<span data-ttu-id="026ad-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="026ad-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="026ad-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="026ad-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="026ad-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="026ad-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="026ad-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="026ad-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

