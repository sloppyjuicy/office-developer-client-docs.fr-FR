---
title: IABContainerDeleteEntries
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.DeleteEntries
api_type:
- COM
ms.assetid: 70a24811-0c41-4b44-8c63-7ef807bc9051
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4140dc39b7f866b0372e5940aef5efc0524ad593
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573109"
---
# <a name="iabcontainerdeleteentries"></a>IABContainer::DeleteEntries

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime une ou plusieurs entrées, généralement autres conteneurs, listes de distribution ou les utilisateurs de messagerie.
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpEntries_
  
> [in] Pointeur vers un tableau de structures [ENTRYLIST](entrylist.md) qui contiennent des identificateurs d’entrée qui représentent les entrées en cours de suppression. 
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les entrées spécifiées ont été supprimées. 
    
MAPI_W_PARTIAL_COMPLETION SE PRODUIT 
  
> L’appel a réussi, mais un ou plusieurs des entrées pas peuvent être supprimé. Lorsque cette valeur est renvoyée, l’appel doit être traité comme étant réussi. Pour tester cette valeur, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|Abdlg.cpp  <br/> |CabDlg::OnDeleteSelectedItem  <br/> |MFCMAPI utilise la méthode **DeleteEntries** pour supprimer une entrée spécifique à partir d’un conteneur de carnet d’adresses.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

