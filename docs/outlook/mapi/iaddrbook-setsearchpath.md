---
title: IAddrBookSetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetSearchPath
api_type:
- COM
ms.assetid: fbff82de-77d3-411e-a30c-a37cefdd92fc
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1d486344ab20ef49488dbb911f3dd7000d64942e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571758"
---
# <a name="iaddrbooksetsearchpath"></a>IAddrBook::SetSearchPath

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Définit un nouveau chemin d’accès de la recherche dans le profil qui est utilisé pour le processus de résolution de nom. 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpSearchPath_
  
> [in] Pointeur vers la structure [SRowSet](srowset.md) utilisée pour contenir le chemin de recherche. La première propriété de chaque membre **: UGAL** dans **SRowSet** doit être **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le chemin de recherche a été défini.
    
MAPI_E_MISSING_REQUIRED_COLUMN 
  
> Un des conteneurs décrites dans la structure **SRowSet** ne comprend pas sa propriété **PR_ENTRYID** . 
    
## <a name="remarks"></a>Remarques

Clients et fournisseurs de services appellent la méthode **SetSearchPath** pour enregistrer les modifications qui ont été apportées à l’ordre de recherche du conteneur qui est utilisé pour résoudre les noms avec la méthode [IAddrBook::ResolveName](iaddrbook-resolvename.md) . Le chemin d’accès de la recherche est enregistrée entre des instances d’une session. 
  
Clients et fournisseurs n’ont pas d’appeler la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) pour conserver les modifications de chemin d’accès de recherche. 
  
## <a name="see-also"></a>Voir aussi



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[Propriété canonique PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

