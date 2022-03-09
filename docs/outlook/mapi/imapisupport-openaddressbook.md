---
title: IMAPISupportOpenAddressBook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.OpenAddressBook
api_type:
- COM
ms.assetid: d8da8be1-3efe-410a-bcce-49e522602d80
ms.openlocfilehash: b49135e716ec97b5c6d0b743b05c195be9443584
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379485"
---
# <a name="imapisupportopenaddressbook"></a>IMAPISupport::OpenAddressBook

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d’accéder au carnet d’adresses.
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a>Paramètres

 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au carnet d’adresses. Les valeurs valides sont NULL, ce qui indique l’interface de carnet d’adresses standard [IAddrBook](iaddrbookimapiprop.md) et IID_IAddrBook.
    
 _ulFlags_
  
> Réservé ; doit être zéro.
    
 _lppAdrBook_
  
> [out] Pointeur vers un pointeur vers le carnet d’adresses.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’accès au carnet d’adresses a été fourni.
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi, mais un ou plusieurs fournisseurs de carnet d’adresses n’ont pas pu être chargés. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED’avertissement** . Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::OpenAddressBook** est implémentée pour tous les objets de prise en charge du fournisseur de services. Les fournisseurs de services, généralement étroitement associés aux fournisseurs de transport et de magasin de messages, appellent **OpenAddressBook** pour accéder au carnet d’adresses. Le **pointeur IAddrBook** renvoyé peut être utilisé pour diverses tâches de carnet d’adresses, notamment l’ouverture de conteneurs de carnet d’adresses, la recherche d’utilisateurs de messagerie et l’affichage de boîtes de dialogue d’adresses. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

 **OpenAddressBook peut** renvoyer MAPI_W_ERRORS_RETURNED s’il ne peut pas charger un ou plusieurs des fournisseurs de carnet d’adresses dans le profil actuel. Cette valeur est un avertissement et vous devez traiter l’appel comme réussi. Même si tous les fournisseurs de carnet d’adresses n’ont pas réussi à se charger, **OpenAddressBook** réussit toujours, renvoyant MAPI_W_ERRORS_RETURNED et un pointeur **IAddrBook** dans le paramètre _lppAdrBook_ . Étant **donné qu’OpenAddressBook** renvoie toujours un pointeur **IAddrBook** valide, vous devez le libérer lorsque vous avez terminé de l’utiliser. 
  
Si un ou plusieurs fournisseurs de carnet d’adresses n’ont pas pu être chargés, appelez [IMAPISupport::GetLastError](imapisupport-getlasterror.md) pour obtenir une structure [MAPIERROR](mapierror.md) qui contient des informations sur les fournisseurs qui n’ont pas été chargés. 
  
## <a name="see-also"></a>Voir aussi



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

