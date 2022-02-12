---
title: IABContainerDeleteEntries
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABContainer.DeleteEntries
api_type:
- COM
ms.assetid: 70a24811-0c41-4b44-8c63-7ef807bc9051
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3256f602576e389a8c7e6103622984870652d2fa
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62772216"
---
# <a name="iabcontainerdeleteentries"></a>IABContainer::DeleteEntries

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime une ou plusieurs entrées, généralement des utilisateurs de messagerie, des listes de distribution ou d’autres conteneurs.
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpEntries_
  
> [in] Pointeur vers un tableau de structures [ENTRYLIST](entrylist.md) qui contiennent des identificateurs d’entrée qui représentent les entrées supprimées. 
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les entrées spécifiées ont été supprimées avec succès. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> L’appel a réussi, mais une ou plusieurs des entrées n’ont pas pu être supprimées. Lorsque cette valeur est renvoyée, l’appel doit être géré comme réussi. Pour tester cette valeur, utilisez la macro **HR_FAILED** macro. Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|Abdlg.cpp  <br/> |CabDlg::OnDeleteSelectedItem  <br/> |MFCMAPI utilise la **méthode DeleteEntries** pour supprimer une entrée spécifique d’un conteneur de carnet d’adresses. |
   
## <a name="see-also"></a>Voir aussi



[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

