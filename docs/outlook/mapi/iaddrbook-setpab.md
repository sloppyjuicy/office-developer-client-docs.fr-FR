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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 29677ce74f405e8ca03f1639f3d98288532e9653
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287013"
---
# <a name="iaddrbooksetpab"></a>IAddrBook::SetPAB

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Désigne un conteneur particulier comme carnet d'adresses personnel (PAB).
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID_
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée du conteneur à désigner comme PAB. Le paramètre _lpEntryID_ ne peut pas être null. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le conteneur spécifié a été défini en tant que PAB.
    
## <a name="remarks"></a>Remarques

Les clients et les fournisseurs de services appellent la méthode **SetPAB** pour désigner un conteneur particulier comme PAB. Le PAB est un conteneur qui se compose d'entrées copiées à partir d'autres conteneurs, ainsi que de nouvelles entrées. 
  
Un appel à **SetPAB** établit un conteneur en tant que PAB jusqu'à ce que ce conteneur soit rendu indisponible ou qu'un nouveau conteneur devienne le PAB via un appel ultérieur à **SetPAB**. 
  
Les clients et les fournisseurs n'ont pas besoin d'appeler la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) pour que le carnet d'un PAB change de façon permanente. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|AbContDlg. cpp  <br/> |CAbContDlg:: OnSetPAB  <br/> |MFCMAPI utilise la méthode **SetPAB** pour définir le conteneur spécifié comme PAB.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[Propriété canonique PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

