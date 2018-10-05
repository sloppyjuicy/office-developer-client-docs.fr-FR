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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6a7bb7265d29d2acfce17a1a09c95f7f7b539064
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396315"
---
# <a name="itnefaddprops"></a>ITnef::AddProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet à l’appelant fournisseur de services ou la passerelle ajouter des propriétés à l’encapsulation d’un message ou d’une pièce jointe. 
  
```cpp
HRESULT AddProps(
  ULONG ulFlags,
  ULONG ulElemID,
  LPVOID lpvData,
  LPSPropTagArray lpPropList
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont les propriétés sont incluses ou exclues d’encapsulation. Les indicateurs suivants peuvent être définis :
    
TNEF_PROP_ATTACHMENTS_ONLY 
  
> Encode les propriétés dans le paramètre _lpPropList_ qui font partie des pièces jointes dans le message. 
    
TNEF_PROP_CONTAINED 
  
> Code uniquement les propriétés de la pièce jointe spécifié par le paramètre _ulElemID_ . Si le paramètre _lpvData_ n’est pas NULL, les données vers lequel pointées sont écrit dans encapsulation de la pièce jointe dans le fichier indiqué par la propriété **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).
    
TNEF_PROP_CONTAINED_TNEF 
  
> Code uniquement les propriétés à partir du message ou d’une pièce jointe spécifié par le paramètre _ulElemID_ . Si cet indicateur est défini, la valeur de _lpvData_ doit être un pointeur [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) . 
    
TNEF_PROP_EXCLUDE 
  
> Code toutes les propriétés non spécifiées dans le paramètre _lpPropList_ . 
    
TNEF_PROP_INCLUDE 
  
> Code toutes les propriétés spécifiées dans _lpPropList_. 
    
TNEF_PROP_MESSAGE_ONLY 
  
> Code uniquement les propriétés spécifiées dans _lpPropList_ qui font partie du message lui-même. 
    
 _ulElemID_
  
> [in] Propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) d’une pièce jointe qui contient un numéro qui identifie de façon unique identifie la pièce jointe dans un message de son parent. Le paramètre _ulElemID_ est utilisé lorsqu’un traitement spécial est demandé pour une pièce jointe. Le paramètre _ulElemID_ doit être 0, sauf si l’indicateur TNEF_PROP_CONTAINED ou TNEF_PROP_CONTAINED_TNEF est défini dans le paramètre _ulFlags_ . 
    
 _lpvData_
  
> [in] Pointeur vers les données de pièce jointe permet de remplacer les données de la pièce jointe spécifiée dans _ulElemID_. Le paramètre _lpvData_ doit être NULL sauf si TNEF_PROP_CONTAINED ou TNEF_PROP_CONTAINED_TNEF est défini dans _ulFlags_.
    
 _lpPropList_
  
> [in] Pointeur vers la liste des propriétés à inclure ou exclure de l’encapsulation.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Fournisseurs de transport, les fournisseurs de banque de message et passerelles appellent la méthode de **ITnef::AddProps** pour les propriétés de la liste pour être inclus ou exclu de la transformation de Transport-Neutral Encapsulation Format (TNEF) d’un message ou d’une pièce jointe. À l’aide des appels successifs, le fournisseur ou la passerelle peut spécifier une liste de propriétés pour ajouter et coder ou à exclure des encodé. Fournisseurs et des passerelles peuvent également utiliser **AddProps** pour fournir plus d’informations sur les pièces jointes d’un traitement spécial doivent être attribués. 
  
 **AddProps** est pris en charge uniquement pour les objets TNEF ouverts avec l’indicateur TNEF_ENCODE pour la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) . 
  
Notez qu’aucun codage TNEF se produit pour **AddProps** jusqu'à ce que la méthode [ITnef::Finish](itnef-finish.md) est appelée. Cette fonctionnalité signifie que des pointeurs transmis à **AddProps** reste valables jusqu'à après l’appel à la **fin** . À ce stade, tous les objets et les données transmises, **AddProps** les appels peuvent être publiées ou libérées. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI utilise la méthode **ITnef::AddProps** pour copier les propriétés d’un message à un flux TNEF.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriété canonique PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

