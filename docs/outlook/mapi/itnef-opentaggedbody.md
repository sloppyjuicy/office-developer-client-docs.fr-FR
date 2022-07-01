---
title: ITnefOpenTaggedBody
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITnef.OpenTaggedBody
api_type:
- COM
ms.assetid: 70d5b34c-85b3-4d1f-860e-2838947ba428
ms.openlocfilehash: 1fd0be3385b48a77a99e14b0f529d59ab093f53d
ms.sourcegitcommit: 600f0dc552b725f98f3354d42feefc39be9c354c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2022
ms.locfileid: "66577342"
---
# <a name="itnefopentaggedbody"></a>ITnef::OpenTaggedBody

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre une interface de flux sur le texte d’un message encapsulé.
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Paramètres

 _lpMessage_
  
> [in] Pointeur vers le message auquel le flux est associé. Ce message n’est pas obligatoire pour être le même message que celui qui est passé dans l’appel à la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) . 
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle la façon dont l’interface de flux est ouverte. Les indicateurs suivants peuvent être définis :
    
MAPI_CREATE 
  
> Si une propriété n’existe pas dans le message actuel, elle doit être créée. Si la propriété existe, les données actuelles de la propriété doivent être remplacées par les données du flux TNEF (Transport-Neutral Encapsulation Format). Lorsqu’une implémentation définit l’indicateur de MAPI_CREATE, elle doit également définir l’indicateur MAPI_MODIFY.
    
MAPI_MODIFY 
  
> Demande l’autorisation de lecture/écriture. L’interface par défaut est en lecture seule. MAPI_MODIFY doit être défini chaque fois que MAPI_CREATE est défini.
    
 _lppStream_
  
> [out] Pointeur vers un pointeur vers un objet de flux qui contient le texte de la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) du message encapsulé passé et qui prend en charge l’interface [IStream](/windows/win32/stg/istream-compound-file-implementation) . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et retourné la valeur ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de transport, les fournisseurs de magasins de messages et les passerelles appellent la méthode **ITnef::OpenTaggedBody** pour ouvrir une interface de flux sur le texte d’un message encapsulé (autrement dit, sur un objet TNEF). 
  
Dans le cadre de son traitement, **OpenTaggedBody** insère ou analyse des balises de pièce jointe qui indiquent la position des pièces jointes ou des objets OLE dans le texte du message. Les balises de pièce jointe sont au format suivant : 
  
 **[[** _nom de pièce jointe_ **:** _n_ **dans le nom du conteneur de** _pièces jointes_ **]]**
  
 _le nom de la pièce jointe_ décrit l’objet pièce jointe ;  _n_ est un nombre qui identifie la pièce jointe qui fait partie d’une séquence, en incrémentant à partir de la valeur passée dans le paramètre _lpKey_ de la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) ; et  _le nom du conteneur de pièces jointes_ décrit le composant physique où réside l’objet pièce jointe. 
  
 **OpenTaggedBody** lit le texte du message et insère une balise de pièce jointe partout où un objet pièce jointe apparaît initialement dans le texte. Le texte du message d’origine n’est pas modifié. 
  
Lorsqu’un message contenant des balises est passé à un flux, les balises sont supprimées et les objets de pièce jointe sont déplacés à la position des balises dans le flux.
  
## <a name="see-also"></a>Voir aussi



[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagBody Canonical, propriété](pidtagbody-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

