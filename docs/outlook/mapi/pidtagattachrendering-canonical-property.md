---
title: Propriété canonique PidTagAttachRendering
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachRendering
api_type:
- HeaderDef
ms.assetid: 1f31f7f4-fbda-4337-95e5-5474dd1bf84a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a1df3ba8e57f1e91894b88d7e8a72feb681e13dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785739"
---
# <a name="pidtagattachrendering-canonical-property"></a><span data-ttu-id="ebd87-103">Propriété canonique PidTagAttachRendering</span><span class="sxs-lookup"><span data-stu-id="ebd87-103">PidTagAttachRendering Canonical Property</span></span>

  
  
<span data-ttu-id="ebd87-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ebd87-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ebd87-105">Contient un métafichier Microsoft Windows avec des informations de rendu d’une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="ebd87-105">Contains a Microsoft Windows metafile with rendering information for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ebd87-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ebd87-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ebd87-107">PR_ATTACH_RENDERING</span><span class="sxs-lookup"><span data-stu-id="ebd87-107">PR_ATTACH_RENDERING</span></span>  <br/> |
|<span data-ttu-id="ebd87-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ebd87-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ebd87-109">0x3709</span><span class="sxs-lookup"><span data-stu-id="ebd87-109">0x3709</span></span>  <br/> |
|<span data-ttu-id="ebd87-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ebd87-110">Data type:</span></span>  <br/> |<span data-ttu-id="ebd87-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ebd87-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ebd87-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="ebd87-112">Area:</span></span>  <br/> |<span data-ttu-id="ebd87-113">Pièce jointe du message</span><span class="sxs-lookup"><span data-stu-id="ebd87-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ebd87-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ebd87-114">Remarks</span></span>

<span data-ttu-id="ebd87-115">L’objectif de cette propriété est de fournir une icône ou une autre représentation graphique qui peut être affichée dans le message parent au moment de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="ebd87-115">The purpose of this property is to provide an icon or other pictorial representation that can be displayed within the parent message at the point of attachment.</span></span> <span data-ttu-id="ebd87-116">Représentation inclut généralement le nom de la pièce jointe, le cas échéant et la nature de la pièce jointe, par exemple un document Microsoft Office Word.</span><span class="sxs-lookup"><span data-stu-id="ebd87-116">Such representation typically includes the name of the attachment, if any, and the nature of the attachment, such as a Microsoft Office Word document.</span></span> <span data-ttu-id="ebd87-117">Une application cliente peut utiliser cette représentation dans l’affichage du message.</span><span class="sxs-lookup"><span data-stu-id="ebd87-117">A client application can use this representation in the display of the message.</span></span> 
  
<span data-ttu-id="ebd87-118">Pour une pièce jointe, cette propriété illustre généralement une icône pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="ebd87-118">For an attached file, this property usually portrays an icon for the file.</span></span> 
  
<span data-ttu-id="ebd87-119">Pour un message attaché, cette propriété n’est généralement pas définie.</span><span class="sxs-lookup"><span data-stu-id="ebd87-119">For an attached message, this property is typically not set.</span></span> <span data-ttu-id="ebd87-120">Une application cliente ayant besoin d’afficher un message joint doit obtenir sa propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), appelez [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) pour un pointeur vers l’objet d’informations de formulaire correspondant, Ouvrez l’interface [IMAPIFormInfo](imapiforminfoimapiprop.md) sur cet objet, puis **GetProps** permet de récupérer les **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) ou la propriété **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ebd87-120">A client application needing to render an attached message should obtain its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) for a pointer to the corresponding form information object, open the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface on that object, and use **GetProps** to retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="ebd87-121">Pour un objet OLE incorporé statique, cette propriété contient un métafichier Microsoft Windows qui peut être utilisé pour dessiner la représentation sous forme de pièce jointe dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ebd87-121">For an embedded static OLE object, this property contains a Microsoft Windows metafile that can be used to draw the attachment representation in a window.</span></span> 
  
<span data-ttu-id="ebd87-122">Pour un objet OLE incorporé dynamique, le client doit utiliser les données OLE pour générer les informations de rendu.</span><span class="sxs-lookup"><span data-stu-id="ebd87-122">For an embedded dynamic OLE object, the client should use the OLE data to generate the rendering information.</span></span> 
  
<span data-ttu-id="ebd87-123">Dans tous les cas, l’application cliente Sachez que cette propriété est généralement plusieurs centaines d’octets de taille et est soumis à la troncation de la table des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="ebd87-123">In all cases, the client application should be aware that this property is usually several hundred bytes in size and is subject to truncation in the attachment table.</span></span> <span data-ttu-id="ebd87-124">Si un client souhaite afficher la pièce jointe à partir de cette propriété sans ouvrir la pièce jointe lui-même, il doit fonctionner dans la règle de troncature de table.</span><span class="sxs-lookup"><span data-stu-id="ebd87-124">If a client wishes to render the attachment from this property without opening the attachment itself, it must work within the table truncation rule.</span></span> <span data-ttu-id="ebd87-125">Pour plus d’informations, voir [utilisation des colonnes de grande taille](working-with-large-columns.md).</span><span class="sxs-lookup"><span data-stu-id="ebd87-125">For more information, see [Working with Large Columns](working-with-large-columns.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ebd87-126">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ebd87-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ebd87-127">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="ebd87-127">Protocol specifications</span></span>

<span data-ttu-id="ebd87-128">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ebd87-128">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ebd87-129">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="ebd87-129">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ebd87-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ebd87-130">Header files</span></span>

<span data-ttu-id="ebd87-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ebd87-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="ebd87-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ebd87-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="ebd87-133">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="ebd87-133">Mapitags.h</span></span>
  
> <span data-ttu-id="ebd87-134">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="ebd87-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ebd87-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebd87-135">See also</span></span>



[<span data-ttu-id="ebd87-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ebd87-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ebd87-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ebd87-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ebd87-138">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ebd87-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ebd87-139">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="ebd87-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

