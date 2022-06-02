---
title: PidLidCustomFlag, propriété canonique
description: Décrit la propriété canonique PidLidCustomFlag, qui est un masque de bits qui spécifie comment un message est personnalisé, par exemple, enregistré avec des propriétés personnalisées.
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
ms.openlocfilehash: ef6502addfd22b7a23005f01b4a9ba60f6b86461
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65853705"
---
# <a name="pidlidcustomflag-canonical-property"></a>PidLidCustomFlag, propriété canonique

**S’applique à** : Outlook 2013 | Outlook 2016
  
Masque de bits qui spécifie comment un message est personnalisé, par exemple, enregistré avec des propriétés personnalisées.

|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |dispidCustomFlag  <br/> |
|ID long (LID) :  <br/> |0x00008251  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |

## <a name="remarks"></a>Remarques

Pour récupérer la valeur de cette propriété, commencez par utiliser **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** pour obtenir la balise de propriété, puis spécifiez cette balise de propriété dans **[IMAPIProp::GetProps](imapiprop-getprops.md)** pour obtenir la valeur.
  
Les indicateurs possibles sont les suivants :
  
****

|**Constante**|**Valeur**|
|:-----|:-----|
|INSP_ONEOFFFLAGS  <br/> |0x0D000000  <br/> |
|INSP_PROPDEFINITION  <br/> |0x02000000  <br/> |

Lors de l’appel **d’IMAPIProp::GetIDsFromNames**, spécifiez les valeurs suivantes pour la structure **[MAPINAMEID](mapinameid.md)** pointée par le paramètre d’entrée *lppPropNames*.
  
****

|**Membre**|**Valeur**|
|:-----|:-----|
|lpGuid :  <br/> |PSETID_Common  <br/> |
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
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.

## <a name="see-also"></a>Voir aussi

[Propriétés MAPI](mapi-properties.md)  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)
