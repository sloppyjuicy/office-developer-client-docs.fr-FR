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
ms.openlocfilehash: 6fed559f0c4af94fcb2b22d1b80b6aa8f1208397
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404607"
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
  
> [in] Pointeur vers le message auquel le flux est associé. Ce message ne doit pas nécessairement être le même message que celui transmis dans l’appel à la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) . 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’interface de flux est ouverte. Les indicateurs suivants peuvent être définies :
    
MAPI_CREATE 
  
> Si une propriété n’existe pas dans le message actuel, elle doit être créée. Si la propriété existe, les données actuelles de la propriété doivent être remplacées par les données du flux TNEF (Transport-Neutral Encapsulation Format). Lorsqu’une implémentation définit l’MAPI_CREATE, elle doit également définir l’MAPI_MODIFY’indicateur.
    
MAPI_MODIFY 
  
> Demande une autorisation de lecture/écriture. L’interface par défaut est en lecture seule. MAPI_MODIFY doit être définie chaque fois que MAPI_CREATE est définie.
    
 _lppStream_
  
> [out] Pointeur vers un pointeur vers un objet de flux qui contient le texte de la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) du message encapsulé transmis et qui prend en charge l’interface [IStream](/windows/desktop/api/objidl/nn-objidl-istream.md) . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et a renvoyé la ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de transport, les fournisseurs de magasins de messages et les passerelles appellent la méthode **ITnef::OpenTaggedBody** pour ouvrir une interface de flux sur le texte d’un message encapsulé (c’est-à-dire, sur un objet TNEF). 
  
Dans le cadre de son traitement, **OpenTaggedBody** insère ou pare les balises de pièce jointe qui indiquent la position des pièces jointes ou des objets OLE dans le texte du message. Les balises de pièce jointe sont au format suivant : 
  
 **[[** _nom de la pièce_ **jointe :** _n dans_ **le nom** _du conteneur de pièces jointes_ **]]**
  
 _le nom de la_ pièce jointe décrit l’objet pièce jointe ;  _n_ est un nombre qui identifie la pièce jointe qui fait partie d’une séquence, incrémentant à partir de la valeur transmise dans le paramètre _lpKey_ de la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) ; et  _le nom du conteneur de_ pièces jointes décrit le composant physique où réside l’objet pièce jointe. 
  
 **OpenTaggedBody** lit le texte du message et insère une balise de pièce jointe là où un objet pièce jointe apparaît dans le texte. Le texte du message d’origine n’est pas modifié. 
  
Lorsqu’un message avec des balises est transmis à un flux, les balises sont vidées et les objets en pièce jointe sont déplacés à la position des balises dans le flux.
  
## <a name="see-also"></a>Voir aussi



[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriété canonique PidTagBody](pidtagbody-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

