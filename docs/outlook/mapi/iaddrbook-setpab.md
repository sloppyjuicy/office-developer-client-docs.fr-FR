---
title: IAddrBookSetPAB
description: Cet article décrit la fonction IAddrBookSetPAB et fournit la syntaxe, les paramètres, la valeur de retour et des remarques supplémentaires.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.SetPAB
api_type:
- COM
ms.assetid: 75daf9d4-6975-435f-91e5-1b41e0047ab7
ms.openlocfilehash: 224cb9e8ddf751e2a8656703d6c49ff1142d1e06
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812333"
---
# <a name="iaddrbooksetpab"></a>IAddrBook::SetPAB

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Désigne un conteneur particulier comme carnet d’adresses personnel (PAB).
  
```cpp
HRESULT SetPAB(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID_
  
> [in] Nombre d’octets dans l’identificateur d’entrée pointé par le paramètre  _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du conteneur à désigner comme PAB. Le paramètre  _lpEntryID_ ne peut pas être NULL. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le conteneur spécifié a été établi en tant que PAB.
    
## <a name="remarks"></a>Remarques

Les clients et les fournisseurs de services appellent la méthode **SetPAB** pour désigner un conteneur particulier en tant que PAB. Le PAB est un conteneur qui se compose d’entrées copiées à partir d’autres conteneurs ainsi que de nouvelles entrées. 
  
Un appel à **SetPAB** établit un conteneur en tant que PAB jusqu’à ce que ce conteneur soit rendu indisponible ou qu’un nouveau conteneur devienne le PAB par le biais d’un appel ultérieur à **SetPAB**. 
  
Les clients et les fournisseurs n’ont pas besoin d’appeler la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) pour rendre la modification PAB permanente. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|AbContDlg.cpp  <br/> |CAbContDlg::OnSetPAB  <br/> |MFCMAPI utilise la méthode **SetPAB** pour faire du conteneur spécifié le PAB. |
   
## <a name="see-also"></a>Voir aussi



[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[Propriété canonique PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

