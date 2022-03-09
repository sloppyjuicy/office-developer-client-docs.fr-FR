---
title: ITnefSetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITnef.SetProps
api_type:
- COM
ms.assetid: 09e4b427-316b-4630-9f3d-81e74f040d7b
ms.openlocfilehash: 8c10dd556ecd54055084191557c2a40146b110b6
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371449"
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
  
> Encode uniquement les propriétés du message ou de la pièce jointe spécifiés par le  _paramètre ulElemID_ . 
    
 _ulElemID_
  
> [in] Propriété **PR_ATTACH_NUM (**[PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) d’une pièce jointe, qui contient un nombre qui identifie de manière unique la pièce jointe dans son message parent.
    
 _cValues_
  
> [in] Nombre de valeurs de propriété dans la structure [SPropValue](spropvalue.md) pointée par  _le paramètre lpProps_ . 
    
 _lpProps_
  
> [in] Pointeur vers une structure **SPropValue** qui contient les valeurs des propriétés à définir. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et a renvoyé la ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de transport, les fournisseurs de magasins de messages et les passerelles appellent la méthode **ITnef::SetProps** pour définir les propriétés à inclure dans l’encapsulation d’un message ou d’une pièce jointe sans modifier le message ou la pièce jointe d’origine. Toutes les propriétés définies avec cet appel remplacent les propriétés existantes dans le message encapsulé. 
  
 **SetProps est** pris en charge uniquement pour les objets TNEF ouverts avec l’indicateur TNEF_ENCODE pour la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) . N’importe quel nombre de propriétés peut être définie avec cet appel. 
  
> [!NOTE]
> Aucun codage TNEF réel pour **SetProps** ne se produit tant que la méthode [ITnef::Finish](itnef-finish.md) n’a pas été appelée. Cette fonctionnalité signifie que les pointeurs passés dans **SetProps** doivent rester valides jusqu’à ce que l’appel à **Finish** soit effectué. À ce stade, tous les objets et données transmis dans les appels **SetProps** peuvent être libérés ou libérés. 
  
## <a name="see-also"></a>Voir aussi



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriété canonique PidTagAttachNumber](pidtagattachnumber-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[ITnef : IUnknown](itnefiunknown.md)

