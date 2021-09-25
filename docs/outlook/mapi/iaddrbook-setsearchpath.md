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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c25bd89d6bc81877a9d5cf9d6b4153081306c2d9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596434"
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
  
> [in] Pointeur vers la structure [SRowSet utilisée](srowset.md) pour contenir le chemin de recherche. La première propriété de chaque **membre aRow** dans **SRowSet** doit être **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le chemin d’accès de recherche a été correctement définie.
    
MAPI_E_MISSING_REQUIRED_COLUMN 
  
> L’un des conteneurs décrits dans la structure **SRowSet** n’inclut pas **sa PR_ENTRYID** propriété. 
    
## <a name="remarks"></a>Remarques

Les clients et les fournisseurs de services appellent la méthode **SetSearchPath** pour enregistrer les modifications qui ont été apportées à l’ordre de recherche de conteneur utilisé pour résoudre les noms avec la méthode [IAddrBook::ResolveName.](iaddrbook-resolvename.md) Le chemin de recherche est enregistré entre les instances d’une session. 
  
Les clients et fournisseurs n’ont pas besoin d’appeler la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) pour rendre permanentes les modifications apportées au chemin de recherche. 
  
## <a name="see-also"></a>Voir aussi



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[Propriété canonique PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

