---
title: Propriété canonique PidLidCustomFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidCustomFlag
api_type:
- COM
ms.assetid: bfb7fd1e-774f-9a2f-fbbe-ba7f68ed8663
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ed5865fe8dfa3a78e91179ac9acbc874ba8f58a6
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375383"
---
# <a name="pidlidcustomflag-canonical-property"></a>Propriété canonique PidLidCustomFlag

**S’applique à** : Outlook 2013 | Outlook 2016
  
Masque de bits qui spécifie la façon dont un message est personnalisé, par exemple, enregistré avec des propriétés personnalisées.

|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidCustomFlag  <br/> |
|ID long (LID) :  <br/> |0x00008251  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |

## <a name="remarks"></a>Remarques

Pour récupérer la valeur de cette propriété, utilisez d’abord **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** pour obtenir la balise de propriété, puis spécifiez cette balise de propriété dans **[IMAPIProp::GetProps](imapiprop-getprops.md)** pour obtenir la valeur.
  
Les indicateurs possibles sont les suivants :
  
****

|**Constante**|**Valeur**|
|:-----|:-----|
|INSP_ONEOFFFLAGS  <br/> |0x0D000000  <br/> |
|INSP_PROPDEFINITION  <br/> |0x02000000  <br/> |

Lorsque vous appelez **IMAPIProp::GetIDsFromNames**, spécifiez les valeurs suivantes pour la structure **[MAPINAMEID](mapinameid.md)** pointée par le paramètre d’entrée *lppPropNames*.
  
****

|**Membre**|**Valeur**|
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind :  <br/> |MNID_ID  <br/> |
|Kind.lID :  <br/> |dispidCustomFlag  <br/> |

## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés.

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
