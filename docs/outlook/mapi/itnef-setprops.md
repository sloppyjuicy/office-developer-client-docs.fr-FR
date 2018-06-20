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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 480a50bd8c3738ad7d0c178cb4cabfdecd15412e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784484"
---
# <a name="itnefsetprops"></a>ITnef::SetProps

  
  
**S’applique à**: Outlook 
  
Définit la valeur d’une ou plusieurs propriétés d’un message encapsulé ou d’une pièce jointe sans modifier le message d’origine ou une pièce jointe. 
  
```cpp
HRESULT SetProps(
  ULONG ulFlags,
  ULONG ulElemID,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont les valeurs de propriété sont définies. Vous pouvez définir l’indicateur suivant :
    
TNEF_PROP_CONTAINED 
  
> Code uniquement les propriétés à partir du message ou d’une pièce jointe spécifié par le paramètre _ulElemID_ . 
    
 _ulElemID_
  
> [in] Propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) d’une pièce jointe qui contient un numéro qui identifie de façon unique identifie la pièce jointe dans un message de son parent.
    
 _cValues_
  
> [in] Le nombre de valeurs de propriété dans la structure [SPropValue](spropvalue.md) indiqué par le paramètre _lpProps_ . 
    
 _lpProps_
  
> [in] Pointeur vers une structure **SPropValue** qui contient des propriétés pour définir les valeurs de propriété. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’appel a réussi et renvoyé la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Transport fournisseurs, les fournisseurs de banque de message et passerelles appel la méthode **ITnef::SetProps** pour définir les propriétés à inclure dans l’encapsulation d’un message ou d’une pièce jointe sans modifier le message d’origine ou la pièce jointe. Toutes les propriétés définies avec cet appel substituent les propriétés existantes dans le message encapsulé. 
  
 **SetProps** est pris en charge uniquement pour les objets TNEF ouverts avec l’indicateur TNEF_ENCODE pour la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) . Nombre de propriétés peut être défini avec cet appel. 
  
> [!NOTE]
> Aucun réel le codage TNEF pour **SetProps** passe-t-il jusqu'à ce que la méthode [ITnef::Finish](itnef-finish.md) est appelée. Cette fonctionnalité signifie que des pointeurs passées dans **SetProps** reste valables jusqu'à après l’appel à la **fin** . À ce stade, tous les objets et les données passées dans **SetProps** appels peuvent être publiées ou libérées. 
  
## <a name="see-also"></a>Voir aussi



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriété canonique PidTagAttachNumber](pidtagattachnumber-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[ITnef : IUnknown](itnefiunknown.md)

