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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0730da9c3877985853e2cd0a55420e64fbd98e0c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342181"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a>IMAPIFormContainer::ResolveMultipleMessageClasses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Résout un groupe de classes de message dans leurs formulaires dans un conteneur de formulaire et renvoie un tableau d'objets d'informations de formulaire pour ces formulaires.
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Paramètres

 _pMsgClassArray_
  
> dans Pointeur vers un tableau qui contient les noms des classes de message à résoudre. Les noms de classe de message sont toujours des chaînes ANSI, jamais Unicode.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle la manière dont les classes de message sont résolues. L'indicateur suivant peut être défini:
    
MAPIFORM_EXACTMATCH 
  
> Seules les chaînes de classe de message correspondant à une correspondance exacte doivent être résolues.
    
 _ppfrminfoarray_
  
> remarquer Pointeur vers un pointeur vers un tableau d'objets d'informations de formulaire. Si une application cliente transmet NULL dans le paramètre _pMsgClassArray_ , le paramètre _ppfrminfoarray_ contient les objets d'informations de formulaire pour tous les formulaires dans le conteneur. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les applications clientes appellent la méthode **IMAPIFormContainer:: ResolveMultipleMessageClasses** pour résoudre un groupe de classes de messages en formulaires dans un conteneur de formulaire. Le tableau des objets d'informations de formulaire renvoyés dans le paramètre _ppfrminfoarray_ fournit un accès supplémentaire à chacune des propriétés des formulaires. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour résoudre un groupe de classes de message en formulaires, transmettez un tableau de noms de classes de message à résoudre. Pour forcer la résolution de façon exacte (autrement dit, pour empêcher la résolution d'une classe de base de la classe de message), l'indicateur MAPIFORM_EXACTMATCH peut être passé dans le paramètre _ulFlags_ . 
  
Si une classe de message ne peut pas être résolue en un formulaire, la valeur NULL est renvoyée pour cette classe de message dans le tableau d'informations sur le formulaire. Par conséquent, même si la méthode renvoie S_OK, ne partez pas du principe que toutes les classes de message ont été résolues avec succès. Au lieu de cela, vérifiez les valeurs du tableau renvoyé.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FormContainerDlg. cpp  <br/> |CFormContainerDlg:: OnResolveMultipleMessageClasses  <br/> |MFCMAPI utilise la méthode **IMAPIFormContainer:: ResolveMultipleMessageClasses** pour localiser un formulaire associé à un ensemble de classes de message.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

