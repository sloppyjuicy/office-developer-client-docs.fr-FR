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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: f7372830624d774fb914ae956e86a9e4476cf487
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315042"
---
# <a name="itnefsetprops"></a>ITnef::SetProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit la valeur d'une ou plusieurs propriétés pour un message encapsulé ou une pièce jointe sans modifier le message ou la pièce jointe d'origine. 
  
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
  
> dans Masque de des indicateurs qui contrôle la manière dont les valeurs des propriétés sont définies. L'indicateur suivant peut être défini:
    
TNEF_PROP_CONTAINED 
  
> Encode uniquement les propriétés du message ou de la pièce jointe spécifiées par le paramètre _ulElemID_ . 
    
 _ulElemID_
  
> dans Propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) d'une pièce jointe, qui contient un numéro qui identifie de manière unique la pièce jointe dans son message parent.
    
 _cValues_
  
> dans Nombre de valeurs de propriété dans la structure [SPropValue](spropvalue.md) vers laquelle pointe le paramètre _lpProps_ . 
    
 _lpProps_
  
> dans Pointeur vers une structure **SPropValue** qui contient les valeurs de propriété des propriétés à définir. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi et a renvoyé la ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de transport, les fournisseurs de banques de messages et les passerelles appellent la méthode **ITnef:: SetProps** pour définir les propriétés à inclure dans l'encapsulation d'un message ou d'une pièce jointe sans modifier le message ou la pièce jointe d'origine. Les propriétés définies avec cet appel remplacent les propriétés existantes dans le message encapsulé. 
  
 **SetProps** est pris en charge uniquement pour les objets TNEF ouverts avec l'indicateur TNEF_ENCODE pour la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) . Il est possible de définir n'importe quel nombre de propriétés avec cet appel. 
  
> [!NOTE]
> Aucun codage TNEF réel n'a lieu pour **SetProps** n'a lieu qu'après l'appel de la méthode [ITnef:: Finish](itnef-finish.md) . Cette fonctionnalité signifie que les pointeurs transmis dans **SetProps** doivent rester valides jusqu'à ce **** que l'appel soit effectué. À ce stade, tous les objets et données transmis aux appels **SetProps** peuvent être libérés ou libérés. 
  
## <a name="see-also"></a>Voir aussi



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriété canonique PidTagAttachNumber](pidtagattachnumber-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[ITnef : IUnknown](itnefiunknown.md)

