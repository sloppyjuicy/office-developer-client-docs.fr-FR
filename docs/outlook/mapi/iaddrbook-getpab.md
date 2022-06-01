---
title: IAddrBookGetPAB
description: L’IAddrBookGetPAB retourne l’identificateur d’entrée du conteneur désigné comme carnet d’adresses personnel (PAB).
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
ms.openlocfilehash: 98b7809280cedb843229e05c61fe615b008aa2c7
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816394"
---
# <a name="iaddrbookgetpab"></a>IAddrBook::GetPAB

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne l’identificateur d’entrée du conteneur désigné comme carnet d’adresses personnel (PAB).
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Paramètres

 _lpcbEntryID_
  
> [out] Pointeur vers le nombre d’octets dans l’identificateur d’entrée pointé par le paramètre  _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée du PAB. Le paramètre  _lppEntryID_ contient zéro si aucun conteneur n’a été désigné comme PAB. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’identificateur d’entrée du PAB a été retourné avec succès.
    
## <a name="remarks"></a>Remarques

Les clients appellent la méthode **GetPAB** pour récupérer l’identificateur d’entrée du conteneur désigné comme PAB. Si un PAB n’a pas été établi dans le profil, MAPI sélectionne comme premier conteneur PAB dans la hiérarchie de carnet d’adresses qui autorise les modifications. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenPAB  <br/> |MFCMAPI utilise la méthode **GetPAB** pour obtenir l’ID du carnet d’adresses personnel de l’utilisateur. |
   
## <a name="see-also"></a>Voir aussi



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriété canonique PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

