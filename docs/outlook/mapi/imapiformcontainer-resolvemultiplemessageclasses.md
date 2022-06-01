---
title: IMAPIFormContainerResolveMultipleMessageClasses
description: IMAPIFormContainerResolveMultipleMessageClasses résout un groupe de classes de message en leurs formulaires dans un conteneur de formulaires et retourne des objets d’informations de formulaire.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormContainer.ResolveMultipleMessageCla
api_type:
- COM
ms.assetid: f18c2dd1-366f-48b4-b335-ebbc0651f467
ms.openlocfilehash: 4f56ffdadebe1e01e99edfe3725dd98419769b40
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815743"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a>IMAPIFormContainer::ResolveMultipleMessageClasses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Résout un groupe de classes de messages en leurs formulaires dans un conteneur de formulaires et retourne un tableau d’objets d’informations de formulaire pour ces formulaires.
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Paramètres

 _pMsgClassArray_
  
> [in] Pointeur vers un tableau qui contient les noms des classes de message à résoudre. Les noms de classes de message sont toujours des chaînes ANSI, jamais Unicode.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont les classes de message sont résolues. L’indicateur suivant peut être défini :
    
MAPIFORM_EXACTMATCH 
  
> Seules les chaînes de classe de message qui correspondent exactement doivent être résolues.
    
 _ppfrminfoarray_
  
> [out] Pointeur vers un pointeur vers un tableau d’objets d’informations de formulaire. Si une application cliente passe null dans le paramètre _pMsgClassArray_ , le paramètre  _ppfrminfoarray_ contient des objets d’informations de formulaire pour tous les formulaires du conteneur. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les applications clientes appellent la méthode **IMAPIFormContainer::ResolveMultipleMessageClasses** pour résoudre un groupe de classes de messages en formulaires dans un conteneur de formulaires. Le tableau d’objets d’informations de formulaire retournés dans le paramètre _ppfrminfoarray_ fournit un accès supplémentaire à chacune des propriétés des formulaires. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour résoudre un groupe de classes de messages en formulaires, transmettez un tableau de noms de classes de message à résoudre. Pour forcer la résolution à être exacte (c’est-à-dire pour empêcher la résolution vers une classe de base de la classe de message), l’indicateur MAPIFORM_EXACTMATCH peut être passé dans le paramètre _ulFlags_ . 
  
Si une classe de message ne peut pas être résolue en formulaire, null est retourné pour cette classe de message dans le tableau d’informations du formulaire. Par conséquent, même si la méthode retourne S_OK, ne partez pas du principe que toutes les classes de message ont été résolues avec succès. Au lieu de cela, vérifiez les valeurs dans le tableau retourné.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMultipleMessageClasses  <br/> |MFCMAPI utilise la méthode **IMAPIFormContainer::ResolveMultipleMessageClasses** pour localiser un formulaire associé à un ensemble de classes de messages. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

