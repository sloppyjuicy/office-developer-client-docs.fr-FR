---
title: IAddrBookGetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetPAB
api_type:
- COM
ms.assetid: 9830e09c-700f-469b-a54d-4e4e0583aa84
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6c565c088fd4ef7d5df141bf770c560f79535998
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349300"
---
# <a name="iaddrbookgetpab"></a>IAddrBook::GetPAB

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie l'identificateur d'entrée du conteneur désigné comme carnet d'adresses personnel (PAB).
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Paramètres

 _lpcbEntryID_
  
> remarquer Pointeur vers le nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lppEntryID_ . 
    
 _lppEntryID_
  
> remarquer Pointeur vers un pointeur vers l'identificateur d'entrée du PAB. Le paramètre _lppEntryID_ contient la valeur zéro si aucun conteneur n'a été désigné comme PAB. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'identificateur d'entrée du PAB a été renvoyé.
    
## <a name="remarks"></a>Remarques

Les clients appellent la méthode **GetPAB** pour récupérer l'identificateur d'entrée du conteneur désigné en tant que PAB. Si un PAB n'a pas été établi dans le profil, MAPI sélectionne comme PAB le premier conteneur de la hiérarchie des carnets d'adresses qui autorise les modifications. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg. cpp  <br/> |CMainDlg:: OnOpenPAB  <br/> |MFCMAPI utilise la méthode **GetPAB** pour obtenir l'ID du carnet d'adresses personnel de l'utilisateur.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriété canonique PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

