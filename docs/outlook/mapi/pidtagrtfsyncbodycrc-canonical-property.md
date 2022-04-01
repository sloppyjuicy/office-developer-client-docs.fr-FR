---
title: Propriété canonique PidTagRtfSyncBodyCrc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRtfSyncBodyCrc
api_type:
- COM
ms.assetid: 95db4837-400f-476f-b313-60e8baa1c6d1
description: Contient la vérification de redondance cyclique (CRC) calculée pour le texte du message. Ces propriétés ne sont pas destinées à être utilisées directement par les applications clientes.
ms.openlocfilehash: ea678d273edb869fe8ddd9c271f3466eaa1692e4
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64523978"
---
# <a name="pidtagrtfsyncbodycrc-canonical-property"></a>Propriété canonique PidTagRtfSyncBodyCrc

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la vérification de redondance cyclique (CRC) calculée pour le texte du message.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RTF_SYNC_BODY_CRC  <br/> |
|Identificateur :  <br/> |0x1006  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Message MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

La [fonction RTFSync](rtfsync.md) calcule la CRC en utilisant uniquement les caractères qu’elle considère comme significatifs pour le message. Par exemple, certains espaces et autres caractères ignoreables sont omis de la CRC. 
  
Cette propriété est une propriété auxiliaire rtf (Rich Text Format). Ces propriétés sont utilisées par **la fonction RTFSync** et ne sont pas destinées à être utilisées directement par les applications clientes. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Code et décode les objets de message et de pièce jointe dans une représentation de flux efficace.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

