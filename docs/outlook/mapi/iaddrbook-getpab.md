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
ms.openlocfilehash: 3d67d71effde87711e3be9aca1b979627acda37d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783635"
---
# <a name="iaddrbookgetpab"></a>IAddrBook::GetPAB

  
  
**S’applique à**: Outlook 
  
Renvoie l’identificateur d’entrée du conteneur qui est désigné comme le carnet d’adresses personnel (CAP).
  
```cpp
HRESULT GetPAB(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Paramètres

 _lpcbEntryID_
  
> [out] Pointeur vers le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée du carnet d’adresses personnel. Le paramètre _lppEntryID_ contient zéro si aucun conteneur n’a été désigné comme le carnet d’adresses personnel. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’identificateur d’entrée du carnet d’adresses personnel a été renvoyée avec succès.
    
## <a name="remarks"></a>Remarques

Les clients appeler la méthode **GetPAB** pour récupérer l’identificateur d’entrée du conteneur désigné comme le carnet d’adresses personnel. Si un carnet d’adresses personnel n’a pas été établie dans le profil, MAPI sélectionne comme le carnet d’adresses personnel le premier conteneur dans la hiérarchie de carnets d’adresses qui permet de modifier. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenPAB  <br/> |MFCMAPI utilise la méthode **GetPAB** pour obtenir l’ID de carnet d’adresses personnel de l’utilisateur.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriété canonique PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

