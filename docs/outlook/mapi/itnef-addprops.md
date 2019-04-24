---
title: ITnefAddProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.AddProps
api_type:
- COM
ms.assetid: e85641fb-6d3c-494a-981c-01781c7bf5bb
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6a7bb7265d29d2acfce17a1a09c95f7f7b539064
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348621"
---
# <a name="itnefaddprops"></a>ITnef::AddProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet au fournisseur de services d'appel ou à la passerelle d'ajouter des propriétés à l'encapsulation d'un message ou d'une pièce jointe. 
  
```cpp
HRESULT AddProps(
  ULONG ulFlags,
  ULONG ulElemID,
  LPVOID lpvData,
  LPSPropTagArray lpPropList
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle la manière dont les propriétés sont incluses ou exclues de l'encapsulation. Les indicateurs suivants peuvent être définis:
    
TNEF_PROP_ATTACHMENTS_ONLY 
  
> Code uniquement les propriétés du paramètre _lpPropList_ qui font partie des pièces jointes dans le message. 
    
TNEF_PROP_CONTAINED 
  
> Encode uniquement les propriétés de la pièce jointe spécifiée par le paramètre _ulElemID_ . Si le paramètre _lpvData_ n'est pas null, les données pointées sur sont écrites dans l'encapsulation de la pièce jointe dans le fichier indiqué par la propriété **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).
    
TNEF_PROP_CONTAINED_TNEF 
  
> Encode uniquement les propriétés du message ou de la pièce jointe spécifiées par le paramètre _ulElemID_ . Si cet indicateur est défini, la valeur dans _lpvData_ doit être un pointeur [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) . 
    
TNEF_PROP_EXCLUDE 
  
> Encode toutes les propriétés non spécifiées dans le paramètre _lpPropList_ . 
    
TNEF_PROP_INCLUDE 
  
> Encode toutes les propriétés spécifiées dans _lpPropList_. 
    
TNEF_PROP_MESSAGE_ONLY 
  
> Encode uniquement les propriétés spécifiées dans _lpPropList_ qui font partie du message lui-même. 
    
 _ulElemID_
  
> dans Propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) d'une pièce jointe, qui contient un numéro qui identifie de manière unique la pièce jointe dans son message parent. Le paramètre _ulElemID_ est utilisé lorsqu'une gestion spéciale est demandée pour une pièce jointe. Le paramètre _ulElemID_ doit être égal à 0 sauf si l'indicateur TNEF_PROP_CONTAINED ou TNEF_PROP_CONTAINED_TNEF est défini dans le paramètre _ulFlags_ . 
    
 _lpvData_
  
> dans Pointeur vers les données de la pièce jointe utilisée pour remplacer les données de la pièce jointe spécifiée dans _ulElemID_. Le paramètre _lpvData_ doit être null, sauf si TNEF_PROP_CONTAINED ou TNEF_PROP_CONTAINED_TNEF est défini dans _ulFlags_.
    
 _lpPropList_
  
> dans Pointeur vers la liste des propriétés à inclure dans l'encapsulation ou à exclure de celle-ci.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de transport, les fournisseurs de banques de messages et les passerelles appellent la méthode **ITnef:: AddProps** pour répertorier les propriétés à inclure dans le traitement TNEF (Transport-Neutral Encapsulation Format) d'un message ou une pièce jointe. En utilisant des appels successifs, le fournisseur ou la passerelle peut spécifier une liste de propriétés à ajouter et encoder ou à exclure de l'encodage. Les fournisseurs et les passerelles peuvent également utiliser **AddProps** pour fournir des informations sur toute manipulation particulière de pièces jointes. 
  
 **AddProps** est pris en charge uniquement pour les objets TNEF ouverts avec l'indicateur TNEF_ENCODE pour la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) . 
  
Notez qu'aucun codage TNEF réel ne se produit pour **AddProps** tant que la méthode [ITnef:: Finish](itnef-finish.md) n'est pas appelée. Cette fonctionnalité signifie que les pointeurs transmis dans **AddProps** doivent rester valides jusqu'à ce **** que l'appel soit effectué. À ce stade, tous les objets et toutes les données transmis avec des appels **AddProps** peuvent être libérés ou libérés. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|File. cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI utilise la méthode **ITnef:: AddProps** pour copier les propriétés d'un message vers un flux TNEF.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriété canonique PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

