---
title: IABContainerDeleteEntries
description: Cet article décrit la fonction IABContainerDeleteEntries et fournit la syntaxe, les paramètres et la valeur de retour.
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
ms.openlocfilehash: 3882b02f41da2b13abbcb05ebbccd94757617018
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816212"
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
  
> L’appel a réussi, mais une ou plusieurs des entrées n’ont pas pu être supprimées. Lorsque cette valeur est retournée, l’appel doit être géré comme ayant réussi. Pour tester cette valeur, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|Abdlg.cpp  <br/> |CabDlg::OnDeleteSelectedItem  <br/> |MFCMAPI utilise la méthode **DeleteEntries** pour supprimer une entrée spécifique d’un conteneur de carnet d’adresses. |
   
## <a name="see-also"></a>Voir aussi



[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

