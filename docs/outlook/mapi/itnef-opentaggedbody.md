---
title: ITnefOpenTaggedBody
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.OpenTaggedBody
api_type:
- COM
ms.assetid: 70d5b34c-85b3-4d1f-860e-2838947ba428
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 154d6e4a4e333f3a6165c3875bdcd57957ebf70c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348733"
---
# <a name="itnefopentaggedbody"></a>ITnef::OpenTaggedBody

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre une interface de flux sur le texte d'un message encapsulé.
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Paramètres

 _lpMessage_
  
> dans Pointeur vers le message auquel le flux est associé. Ce message ne doit pas obligatoirement être le même message que celui transmis dans l'appel à la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) . 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle la manière dont l'interface de flux est ouverte. Les indicateurs suivants peuvent être définis:
    
MAPI_CREATE 
  
> Si une propriété n'existe pas dans le message actif, elle doit être créée. Si la propriété existe, les données actuelles de la propriété doivent être remplacées par les données du flux TNEF (Transport-Neutral Encapsulation Format). Lorsqu'une implémentation définit l'indicateur MAPI_CREATE, elle doit également définir l'indicateur MAPI_MODIFY.
    
MAPI_MODIFY 
  
> Demande une autorisation en lecture/écriture. L'interface par défaut est en lecture seule. MAPI_MODIFY doit être défini à chaque fois que MAPI_CREATE est défini.
    
 _lppStream_
  
> remarquer Pointeur vers un pointeur vers un objet Stream qui contient le texte de la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) du message encapsulé transmis et qui prend en charge l'interface [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi et a renvoyé la ou les valeurs attendues.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de transport, les fournisseurs de banques de messages et les passerelles appellent la méthode **ITnef:: OpenTaggedBody** pour ouvrir une interface de flux sur le texte d'un message encapsulé (c'est-à-dire sur un objet TNEF). 
  
Dans le cadre de son traitement, **OpenTaggedBody** insère ou analyse les balises de pièce jointe qui indiquent la position des pièces jointes ou des objets OLE dans le texte du message. Les balises de pièces jointes sont au format suivant: 
  
 **[[** _nom de la pièce jointe_ **:** _n_ **dans le nom du conteneur de** _pièces jointes_ **]]**
  
 _nom_ de la pièce jointe décrit l'objet Attachment;  _n_ est un nombre qui identifie la pièce jointe qui fait partie d'une séquence, incrémentant à partir de la valeur transmise dans le paramètre _lpKey_ de la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) ; et _nom du conteneur de pièces jointes_ décrit le composant physique où réside l'objet pièce jointe. 
  
 **OpenTaggedBody** lit le texte du message et insère une balise de pièce jointe à l'emplacement où un objet pièce jointe s'affichait à l'origine dans le texte. Le texte du message d'origine n'est pas modifié. 
  
Lorsqu'un message comportant des balises est transmis à un objet Stream, les balises sont supprimées et les objets Attachment sont déplacés dans la position des balises dans le flux.
  
## <a name="see-also"></a>Voir aussi



[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriété canonique PidTagBody](pidtagbody-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

