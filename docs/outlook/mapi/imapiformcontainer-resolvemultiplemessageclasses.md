---
title: IMAPIFormContainerResolveMultipleMessageClasses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMultipleMessageCla
api_type:
- COM
ms.assetid: f18c2dd1-366f-48b4-b335-ebbc0651f467
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0730da9c3877985853e2cd0a55420e64fbd98e0c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412540"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a>IMAPIFormContainer::ResolveMultipleMessageClasses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Résout un groupe de classes de message dans leurs formulaires dans un conteneur de formulaires et renvoie un tableau d’objets d’informations de formulaire pour ces formulaires.
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Parameters

 _pMsgClassArray_
  
> [in] Pointeur vers un tableau qui contient les noms des classes de message à résoudre. Les noms de classe de message sont toujours des chaînes ANSI, jamais Unicode.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont les classes de message sont résolues. L’indicateur suivant peut être définie :
    
MAPIFORM_EXACTMATCH 
  
> Seules les chaînes de classe de message qui correspondent exactement doivent être résolues.
    
 _ppfrminfoarray_
  
> [out] Pointeur vers un pointeur vers un tableau d’objets d’informations de formulaire. Si une application cliente transmet la valeur NULL dans le paramètre  _pMsgClassArray,_ le paramètre  _ppfrminfoarray_ contient des objets d’informations de formulaire pour tous les formulaires dans le conteneur. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les applications clientes appellent la méthode **IMAPIFormContainer::ResolveMultipleMessageClasses** pour résoudre un groupe de classes de message en formulaires dans un conteneur de formulaires. Le tableau des objets d’informations de formulaire renvoyés dans le paramètre  _ppfrminfoarray_ fournit un accès supplémentaire à chacune des propriétés des formulaires. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour résoudre un groupe de classes de message en formulaires, passez un tableau de noms de classes de messages à résoudre. Pour forcer la résolution à être exacte (c’est-à-dire pour empêcher la résolution à une classe de base de la classe de message), l’indicateur MAPIFORM_EXACTMATCH peut être transmis dans le paramètre _ulFlags._ 
  
Si une classe de message ne peut pas être résolue en formulaire, null est renvoyé pour cette classe de message dans le tableau d’informations du formulaire. Par conséquent, même si la méthode renvoie S_OK, ne supposez pas que toutes les classes de message ont été correctement résolues. Vérifiez plutôt les valeurs dans le tableau renvoyé.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMultipleMessageClasses  <br/> |MFCMAPI utilise la méthode **IMAPIFormContainer::ResolveMultipleMessageClasses** pour localiser un formulaire associé à un ensemble de classes de messages.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

