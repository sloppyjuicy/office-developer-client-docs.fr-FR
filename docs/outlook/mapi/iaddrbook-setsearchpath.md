---
title: IAddrBookSetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.SetSearchPath
api_type:
- COM
ms.assetid: fbff82de-77d3-411e-a30c-a37cefdd92fc
ms.openlocfilehash: 538d58149e4cddfbcdd42054ee7f43c0374a6fac
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63382131"
---
# <a name="iaddrbooksetsearchpath"></a>IAddrBook::SetSearchPath

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit un nouveau chemin de recherche dans le profil utilisé pour le processus de résolution de noms. 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpSearchPath_
  
> [in] Pointeur vers la structure [SRowSet](srowset.md) utilisée pour contenir le chemin de recherche. La première propriété de chaque **membre aRow** dans **SRowSet** doit être **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le chemin d’accès de recherche a été correctement définie.
    
MAPI_E_MISSING_REQUIRED_COLUMN 
  
> L’un des conteneurs décrits dans la structure **SRowSet** n’incluait pas **sa PR_ENTRYID** propriété. 
    
## <a name="remarks"></a>Remarques

Les clients et les fournisseurs de services appellent la méthode **SetSearchPath** pour enregistrer les modifications qui ont été apportées à l’ordre de recherche de conteneur utilisé pour résoudre les noms avec la méthode [IAddrBook::ResolveName](iaddrbook-resolvename.md) . Le chemin de recherche est enregistré entre les instances d’une session. 
  
Les clients et fournisseurs n’ont pas besoin d’appeler la méthode [IMAPIProp::SaveChanges pour rendre permanentes les modifications apportées](imapiprop-savechanges.md) au chemin de recherche. 
  
## <a name="see-also"></a>Voir aussi



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[Propriété canonique PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

