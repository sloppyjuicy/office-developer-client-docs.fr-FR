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
ms.openlocfilehash: 002dbf3e898fc0388d535e3087d17ba37d63201e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577708"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a>IMAPIFormContainer::ResolveMultipleMessageClasses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Résout un groupe de classes de message à leurs formulaires dans un conteneur de formulaire et renvoie un tableau de formulaire objets des informations pour les formulaires.
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Paramètres

 _pMsgClassArray_
  
> [in] Pointeur vers un tableau qui contient les noms des classes de message à résoudre. Noms de classe de message sont toujours des chaînes ANSI, Unicode jamais.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont les classes de message sont résolus. Vous pouvez définir l’indicateur suivant :
    
MAPIFORM_EXACTMATCH 
  
> Seules les chaînes de classe de message qui sont une correspondance exacte doivent être résolus.
    
 _ppfrminfoarray_
  
> [out] Pointeur vers un pointeur vers un tableau d’objets d’informations de formulaire. Si une application cliente passe NULL dans le paramètre _pMsgClassArray_ , le paramètre _ppfrminfoarray_ contient des objets d’informations de formulaire pour tous les formulaires dans le conteneur. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Applications clientes appellent la méthode **IMAPIFormContainer::ResolveMultipleMessageClasses** pour résoudre un groupe de classes de message pour des formulaires dans un conteneur de formulaire. Le tableau d’objets retournés dans le paramètre _ppfrminfoarray_ formulaire fournit davantage l’accès à chacune des propriétés des formulaires. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Pour résoudre un groupe de classes de message aux formulaires, passez un tableau de résolution des noms de classe de message. Pour forcer la résolution à être exact (autrement dit, pour empêcher la résolution à une classe de base de la classe de message), l’indicateur MAPIFORM_EXACTMATCH peut être passé dans le paramètre _ulFlags_ . 
  
Si une classe de message ne peut pas être résolue à un formulaire, NULL est renvoyé pour cette classe de message dans le tableau d’informations de formulaire. Par conséquent, même si la méthode renvoie S_OK, ne supposent que toutes les classes de message ont été correctement résolus. Au lieu de cela, vérifiez les valeurs dans le tableau retourné.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMultipleMessageClasses  <br/> |MFCMAPI utilise la méthode **IMAPIFormContainer::ResolveMultipleMessageClasses** pour localiser un formulaire qui est associé à un ensemble de classes de message.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

