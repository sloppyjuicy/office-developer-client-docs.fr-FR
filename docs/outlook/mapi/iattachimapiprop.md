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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2ef3bc973e12bd5630cc00b3c512b748d4a16e86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409089"
---
# <a name="iattach--imapiprop"></a>IAttach : IMAPIProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Conserve et permet d'accéder aux propriétés des pièces jointes dans les messages. L'interface **IAttach** ne possède pas de méthodes uniques. Pour plus d'informations sur l'utilisation des pièces jointes, consultez la rubrique [MAPI Attachments](mapi-attachments.md) and [Attachment tables](attachment-tables.md). 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Exposé par:  <br/> |Objets Attachment  <br/> |
|Implémenté par :  <br/> |Fournisseurs de banques de messages  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur de l'interface:  <br/> |IID_IAttachment  <br/> |
|Type de pointeur:  <br/> |LPATTACH  <br/> |
|Modèle de transaction:  <br/> |Traitées  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

Cette interface n'a pas de méthodes uniques.
  
|**Propriétés requises**|**Accès**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Lecture seule  <br/> |
|**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))  <br/> |Lecture/écriture  <br/> |
|**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |Lecture/écriture  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

