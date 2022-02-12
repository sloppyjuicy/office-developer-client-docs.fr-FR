---
title: IAddrBookGetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.GetPAB
api_type:
- COM
ms.assetid: 9830e09c-700f-469b-a54d-4e4e0583aa84
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7f4939a25cc7012037d7d1dbfe450250c98f28f2
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773564"
---
# <a name="iaddrbookgetpab"></a>IAddrBook::GetPAB

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie l’identificateur d’entrée du conteneur désigné comme carnet d’adresses personnel .
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Paramètres

 _lpcbEntryID_
  
> [out] Pointeur vers le nombre d’byte dans l’identificateur d’entrée pointé par  _le paramètre lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée du PAB. Le  _paramètre lppEntryID_ contient zéro si aucun conteneur n’a été désigné comme PAB. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’identificateur d’entrée du PAB a été renvoyé avec succès.
    
## <a name="remarks"></a>Remarques

Les clients appellent **la méthode GetPAB** pour récupérer l’identificateur d’entrée du conteneur désigné comme PAB. Si un carnet d’adresses en mode page n’a pas été établi dans le profil, MAPI sélectionne comme carnet d’adresses en mode page le premier conteneur dans la hiérarchie de carnet d’adresses qui autorise les modifications. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenPAB  <br/> |MFCMAPI utilise la **méthode GetPAB** pour obtenir l’ID du carnet d’adresses personnel de l’utilisateur. |
   
## <a name="see-also"></a>Voir aussi



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriété canonique PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

