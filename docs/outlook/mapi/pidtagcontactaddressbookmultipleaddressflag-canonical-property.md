---
title: Propriété canonique PidTagContactAddressBookMultipleAddressFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContactAddressBookMultipleAddressFlag
api_type:
- HeaderDef
ms.assetid: aefc34c5-1beb-44cf-a455-90f466e157ce
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3479b7218ad09f41cf137bb8d574ad501ebe3533
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63725978"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a>Propriété canonique PidTagContactAddressBookMultipleAddressFlag

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un indicateur true lorsque le fournisseur prend en charge plusieurs adresses de messagerie par élément de contact.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTAB_MULTI_ADDR_FLAG  <br/> |
|Identificateur :  <br/> |0x6614  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Carnet d’adresses de contact  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété a la valeur TRUE, le fournisseur n’autorise pas les contacts sans adresse de messagerie. Si la false, le fournisseur indique à tous les contacts s’ils ont ou non une adresse de messagerie principale. Seule l’adresse de messagerie principale sera honorée. Il s’agit d’une propriété d’un conteneur de carnet d’adresses de contact et d’une colonne dans la table des conteneurs de carnet d’adresses de contact.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

