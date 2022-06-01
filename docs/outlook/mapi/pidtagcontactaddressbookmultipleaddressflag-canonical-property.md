---
title: Propriété canonique PidTagContactAddressBookMultipleAddressFlag
description: Décrit la propriété canonique PidTagContactAddressBookMultipleAddressFlag, qui est TRUE si le fournisseur n’autorise pas les contacts sans adresse e-mail.
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
ms.openlocfilehash: dc480ec6b42afe6313ab7b79fbed7268635cd840
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65811815"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a>Propriété canonique PidTagContactAddressBookMultipleAddressFlag

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un indicateur true lorsque le fournisseur prend en charge plusieurs adresses e-mail par élément de contact.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTAB_MULTI_ADDR_FLAG  <br/> |
|Identificateur :  <br/> |0x6614  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Carnet d’adresses de contact  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété est TRUE, le fournisseur n’autorise pas les contacts sans adresse e-mail. Si la valeur est FALSE, le fournisseur affiche tous les contacts, qu’ils aient ou non une adresse e-mail principale. Seule l’adresse e-mail principale sera honorée. Il s’agit d’une propriété sur un conteneur de carnets d’adresses de contact et d’une colonne dans la table des conteneurs de carnets d’adresses de contact.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

