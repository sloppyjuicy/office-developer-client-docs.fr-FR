---
title: IAddrBookSetPAB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetPAB
api_type:
- COM
ms.assetid: 75daf9d4-6975-435f-91e5-1b41e0047ab7
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 461b59ff4f4c8a93f3a9945b05e31aef9a2997bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569301"
---
# <a name="iaddrbooksetpab"></a>IAddrBook::SetPAB

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Désigne un conteneur spécifique comme le carnet d’adresses personnel (CAP).
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du conteneur à désigner comme le carnet d’adresses personnel. Le paramètre _lpEntryID_ ne peut pas être NULL. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le conteneur spécifié a été établi en tant que le carnet d’adresses personnel.
    
## <a name="remarks"></a>Remarques

Clients et fournisseurs de services appellent la méthode **SetPAB** pour désigner un conteneur spécifique comme le carnet d’adresses personnel. Le carnet d’adresses personnel est un conteneur qui se compose d’entrées copiées à partir d’autres conteneurs, ainsi que les nouvelles entrées. 
  
Un appel à **SetPAB** établit un conteneur en tant que le carnet d’adresses personnel jusqu'à ce que ce conteneur devient indisponible, ou un nouveau conteneur devient le carnet d’adresses personnel via un autre appel à **SetPAB**. 
  
Clients et fournisseurs n’ont pas d’appeler la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) pour conserver le changement de carnet d’adresses personnel. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|AbContDlg.cpp  <br/> |CAbContDlg::OnSetPAB  <br/> |MFCMAPI utilise la méthode **SetPAB** pour effectuer le conteneur spécifié le carnet d’adresses personnel.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[Propriété canonique PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

