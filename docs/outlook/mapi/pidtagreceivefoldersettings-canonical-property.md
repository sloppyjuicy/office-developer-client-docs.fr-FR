---
title: Propriété canonique PidTagReceiveFolderSettings
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceiveFolderSettings
api_type:
- COM
ms.assetid: 2f0b1679-05b0-4580-b6d2-474fe3f9d012
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e93325873f1d9e89bb591d136df04aa27403375f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786524"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a><span data-ttu-id="d9786-103">Propriété canonique PidTagReceiveFolderSettings</span><span class="sxs-lookup"><span data-stu-id="d9786-103">PidTagReceiveFolderSettings Canonical Property</span></span>

  
  
<span data-ttu-id="d9786-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d9786-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d9786-105">Contient un tableau d’un message de la banque de recevoir des paramètres du dossier.</span><span class="sxs-lookup"><span data-stu-id="d9786-105">Contains a table of a message store's receive folder settings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d9786-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d9786-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d9786-107">PR_RECEIVE_FOLDER_SETTINGS</span><span class="sxs-lookup"><span data-stu-id="d9786-107">PR_RECEIVE_FOLDER_SETTINGS</span></span>  <br/> |
|<span data-ttu-id="d9786-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d9786-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d9786-109">0x3415</span><span class="sxs-lookup"><span data-stu-id="d9786-109">0x3415</span></span>  <br/> |
|<span data-ttu-id="d9786-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d9786-110">Data type:</span></span>  <br/> |<span data-ttu-id="d9786-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="d9786-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="d9786-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="d9786-112">Area:</span></span>  <br/> |<span data-ttu-id="d9786-113">Banque de messages MAPI</span><span class="sxs-lookup"><span data-stu-id="d9786-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9786-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d9786-114">Remarks</span></span>

<span data-ttu-id="d9786-115">Cette propriété peut être exclue dans les opérations [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluse dans les opérations de [IMAPIProp::CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="d9786-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="d9786-116">En tant que propriété de type PT_OBJECT, il ne peut pas être récupéré par la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) ; son contenu doit être accessible par la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , qui demande à l’interface avec l’identificateur IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="d9786-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the interface with identifier IID_IMAPITable.</span></span> <span data-ttu-id="d9786-117">Fournisseurs de services doivent signaler à la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) s’il est défini, mais peut le signaler ou pas si elle n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="d9786-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="d9786-118">Pour récupérer le contenu du tableau, une application cliente doit appeler la méthode [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) .</span><span class="sxs-lookup"><span data-stu-id="d9786-118">To retrieve table contents, a client application should call the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> <span data-ttu-id="d9786-119">Pour plus d’informations, voir [S’afficher les Tables de dossier](receive-folder-tables.md).</span><span class="sxs-lookup"><span data-stu-id="d9786-119">For more information, see [Receive Folder Tables](receive-folder-tables.md).</span></span>
  
<span data-ttu-id="d9786-120">Cette propriété contient une table de mappages de dossiers receive pour la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="d9786-120">This property contains a table of mappings of the receive folders for the message store.</span></span> <span data-ttu-id="d9786-121">L’appel **OpenProperty** sur cette propriété est équivalente à l’appel **GetReceiveFolderTable** sur la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="d9786-121">Calling **OpenProperty** on this property is equivalent to calling **GetReceiveFolderTable** on the message store.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d9786-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d9786-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d9786-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d9786-123">Header files</span></span>

<span data-ttu-id="d9786-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d9786-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="d9786-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d9786-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="d9786-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="d9786-126">Mapitags.h</span></span>
  
> <span data-ttu-id="d9786-127">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="d9786-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9786-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9786-128">See also</span></span>



[<span data-ttu-id="d9786-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d9786-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d9786-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d9786-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d9786-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d9786-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d9786-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="d9786-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

