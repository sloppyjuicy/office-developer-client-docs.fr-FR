---
title: ITnefSetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.SetProps
api_type:
- COM
ms.assetid: 09e4b427-316b-4630-9f3d-81e74f040d7b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f7372830624d774fb914ae956e86a9e4476cf487
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430790"
---
# <a name="itnefsetprops"></a>ITnef::SetProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit la valeur d’une ou de plusieurs propriétés d’un message ou d’une pièce jointe encapsulé sans modifier le message ou la pièce jointe d’origine. 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont les valeurs des propriétés sont définies. L’indicateur suivant peut être définie :
    
TNEF_PROP_CONTAINED 
  
> Encode uniquement les propriétés du message ou de la pièce jointe spécifiés par le _paramètre ulElemID._ 
    
 _ulElemID_
  
> [in] Propriété de PR_ATTACH_NUM **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)), qui contient un nombre qui identifie de manière unique la pièce jointe dans son message parent.
    
 _cValues_
  
> [in] Nombre de valeurs de propriété dans la structure [SPropValue](spropvalue.md) pointée par _le paramètre lpProps._ 
    
 _lpProps_
  
> [in] Pointeur vers une structure **SPropValue** qui contient les valeurs des propriétés à définir. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et a renvoyé la ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de transport, les fournisseurs de magasins de messages et les passerelles appellent la méthode **ITnef::SetProps** pour définir les propriétés à inclure dans l’encapsulation d’un message ou d’une pièce jointe sans modifier le message ou la pièce jointe d’origine. Toutes les propriétés définies avec cet appel remplacent les propriétés existantes dans le message encapsulé. 
  
 **SetProps est** pris en charge uniquement pour les objets TNEF ouverts avec l’indicateur TNEF_ENCODE pour la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx.](opentnefstreamex.md) N’importe quel nombre de propriétés peut être définie avec cet appel. 
  
> [!NOTE]
> Aucun codage TNEF réel pour **SetProps** ne se produit tant que la méthode [ITnef::Finish](itnef-finish.md) n’a pas été appelée. Cette fonctionnalité signifie que les pointeurs passés dans **SetProps** doivent rester valides jusqu’à ce que l’appel à **Finish** soit effectué. À ce stade, tous les objets et données transmis dans les appels **SetProps** peuvent être libérés ou libérés. 
  
## <a name="see-also"></a>Voir aussi



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriété canonique PidTagAttachNumber](pidtagattachnumber-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[ITnef : IUnknown](itnefiunknown.md)

