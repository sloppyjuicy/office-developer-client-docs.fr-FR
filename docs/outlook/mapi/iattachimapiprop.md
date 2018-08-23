---
title: IAttach IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttach
api_type:
- COM
ms.assetid: f47e20e1-2a30-4c9e-8ca6-e8c5e72f44a1
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ce9c8b189991e4102fcc9d17b88747d4ce55efec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570911"
---
# <a name="iattach--imapiprop"></a>IAttach : IMAPIProp

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Gère et donne accès aux propriétés des pièces jointes des messages. L’interface **IAttach** a aucune méthode unique qui lui est propre. Pour plus d’informations sur l’utilisation des pièces jointes, voir [Les pièces jointes MAPI](mapi-attachments.md) et les [Tables des pièces jointes](attachment-tables.md). 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposés par :  <br/> |Objets Attachment  <br/> |
|Implémentée par :  <br/> |Fournisseurs de banque de messages  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
|Identificateur de l’interface :  <br/> |IID_IAttachment  <br/> |
|Type de pointeur :  <br/> |LPATTACH  <br/> |
|Modèle de transaction :  <br/> |Traitées  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

Cette interface n’a pas de méthodes uniques.
  
|**Propriétés requises**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))  <br/> |En lecture-écriture.  <br/> |
|**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |En lecture-écriture.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

