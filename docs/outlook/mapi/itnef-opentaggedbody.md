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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 154d6e4a4e333f3a6165c3875bdcd57957ebf70c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383740"
---
# <a name="itnefopentaggedbody"></a>ITnef::OpenTaggedBody

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
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
  
> [in] Pointeur vers le message auquel l’objet stream est associé. Ce message n’est pas requis pour être le même message est passé dans l’appel à la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) . 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’interface du flux est ouvert. Les indicateurs suivants peuvent être définis :
    
MAPI_CREATE 
  
> Si une propriété n’existe pas dans le message en cours, il doit être créé. Si la propriété n’existe pas, les données actuelles de la propriété doivent être remplacées par les données à partir du flux de Transport-Neutral Encapsulation Format (TNEF). Lorsqu’une implémentation définit l’indicateur MAPI_CREATE, il doit également affecter l’indicateur ne.
    
N' 
  
> Demandes d’autorisation de lecture/écriture. L’interface par défaut est en lecture seule. Ne doit être définie chaque fois que MAPI_CREATE est défini.
    
 _lppStream_
  
> [out] Un pointeur vers un pointeur vers un objet stream qui contient le texte de la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) du passé en encapsulé message et qui prend en charge l’interface [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et renvoyé la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Fournisseurs de transport, les fournisseurs de banque de message et passerelles appellent la méthode **ITnef::OpenTaggedBody** pour ouvrir une interface de flux sur le texte d’un message encapsulé (autrement dit, un TNEF d’objets). 
  
Dans le cadre de son traitement, **OpenTaggedBody** insère ou analyse des balises de pièce jointe qui indiquent la position des pièces jointes ou les objets OLE dans le texte du message. Les balises de pièce jointe sont dans le format suivant : 
  
 **[[** ** _nom de la pièce jointe_ **:** _n_ _nom de conteneur de pièce jointe_ ** **]]**
  
 _nom de la pièce jointe_ décrit l’objet de pièce jointe ;  _n_ est un numéro qui identifie la pièce jointe qui fait partie d’une séquence, s’incrémentant à partir de la valeur passée dans le paramètre _lpKey_ du [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) fonction ; et _le nom de conteneur pièce jointe_ décrit le composant physique où réside l’objet attachment. 
  
 **OpenTaggedBody** lit le texte du message et insère une balise de pièce jointe partout où un objet attachment s’affichait dans le texte. Le texte du message d’origine n’est pas modifié. 
  
Lorsqu’un message qui comporte des balises est passé à un flux de données, les balises sont supprimés et les objets attachment sont déplacés dans la position des balises dans le flux.
  
## <a name="see-also"></a>Voir aussi



[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriété canonique PidTagBody](pidtagbody-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

