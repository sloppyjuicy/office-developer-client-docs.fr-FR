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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348621"
---
# <a name="itnefaddprops"></a>ITnef::AddProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet au fournisseur de services d’appel ou à la passerelle d’ajouter des propriétés à l’encapsulation d’un message ou d’une pièce jointe. 
  
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
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont les propriétés sont incluses ou exclues de l’encapsulation. Les indicateurs suivants peuvent être définies :
    
TNEF_PROP_ATTACHMENTS_ONLY 
  
> Encode uniquement les propriétés du  _paramètre lpPropList_ qui font partie des pièces jointes dans le message. 
    
TNEF_PROP_CONTAINED 
  
> Encode uniquement les propriétés de la pièce jointe spécifiée par _le paramètre ulElemID._ Si le paramètre  _lpvData_ n’est pas NULL, les données pointées vers sont écrites dans l’encapsulation de la pièce jointe dans le fichier indiqué par la propriété **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).
    
TNEF_PROP_CONTAINED_TNEF 
  
> Encode uniquement les propriétés du message ou de la pièce jointe spécifiés par le _paramètre ulElemID._ Si cet indicateur est définie, la valeur dans _lpvData_ doit être un [pointeur IStream.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) 
    
TNEF_PROP_EXCLUDE 
  
> Encode toutes les propriétés non spécifiées dans _le paramètre lpPropList._ 
    
TNEF_PROP_INCLUDE 
  
> Encode toutes les propriétés spécifiées dans  _lpPropList_. 
    
TNEF_PROP_MESSAGE_ONLY 
  
> Encode uniquement les propriétés spécifiées dans  _lpPropList_ qui font partie du message lui-même. 
    
 _ulElemID_
  
> [in] Propriété de PR_ATTACH_NUM **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)), qui contient un nombre qui identifie de manière unique la pièce jointe dans son message parent. Le  _paramètre ulElemID_ est utilisé lorsque la gestion spéciale d’une pièce jointe est demandée. Le _paramètre ulElemID_ doit être 0, sauf si l’indicateur TNEF_PROP_CONTAINED ou TNEF_PROP_CONTAINED_TNEF est définie dans le _paramètre ulFlags._ 
    
 _lpvData_
  
> [in] Pointeur vers les données de pièce jointe utilisées pour remplacer les données de la pièce jointe spécifiée dans  _ulElemID_. Le  _paramètre lpvData_ doit être NULL, sauf si TNEF_PROP_CONTAINED ou TNEF_PROP_CONTAINED_TNEF est définie dans  _ulFlags_.
    
 _lpPropList_
  
> [in] Pointeur vers la liste des propriétés à inclure ou à exclure de l’encapsulation.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de transport, les fournisseurs de magasins de messages et les passerelles appellent la méthode **ITnef::AddProps** pour ré lister les propriétés à inclure ou à exclure du traitement TNEF (Transport-Neutral Encapsulation Format) d’un message ou d’une pièce jointe. À l’aide d’appels successifs, le fournisseur ou la passerelle peut spécifier une liste de propriétés à ajouter et coder ou à exclure de l’encodage. Les fournisseurs et passerelles peuvent également utiliser **AddProps** pour fournir des informations sur toute gestion spéciale des pièces jointes. 
  
 **AddProps est** pris en charge uniquement pour les objets TNEF ouverts avec l’indicateur TNEF_ENCODE pour la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx.](opentnefstreamex.md) 
  
Notez qu’aucun codage TNEF réel ne se produit pour **AddProps** tant que la méthode [ITnef::Finish](itnef-finish.md) n’est pas appelée. Cette fonctionnalité signifie que les pointeurs passés dans **AddProps** doivent rester valides jusqu’à la fin de **l’appel.** À ce stade, tous les objets et données transmis avec les appels **AddProps** peuvent être libérés ou libérés. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI utilise la méthode **ITnef::AddProps** pour copier les propriétés d’un message vers un flux TNEF.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propriété canonique PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

