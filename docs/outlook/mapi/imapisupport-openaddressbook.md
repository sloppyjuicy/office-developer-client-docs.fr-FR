---
title: IMAPISupportOpenAddressBook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenAddressBook
api_type:
- COM
ms.assetid: d8da8be1-3efe-410a-bcce-49e522602d80
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 26550691ef959fa7cefa83827dd1391538bd2d38
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588173"
---
# <a name="imapisupportopenaddressbook"></a>IMAPISupport::OpenAddressBook

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit l’accès au carnet d’adresses.
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a>Paramètres

 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au carnet d’adresses. Les valeurs valides sont NULL, ce qui indique l’interface de carnet d’adresses standard [IAddrBook](iaddrbookimapiprop.md)et IID_IAddrBook.
    
 _ulFlags_
  
> Réservé ; doit être égal à zéro.
    
 _lppAdrBook_
  
> [out] Pointeur vers un pointeur vers le carnet d’adresses.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Accès au carnet d’adresses a été fournie.
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi, mais un ou plusieurs fournisseurs de carnet d’adresses n’a pas peuvent être chargés. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::OpenAddressBook** est implémentée pour tous les objets de prise en charge de fournisseur de service. Fournisseurs de services, généralement étroitement couplé message stockent et fournisseurs de transport, appelez **OpenAddressBook** pour obtenir l’accès au carnet d’adresses. Le pointeur de **IAddrBook** retourné peut être utilisé pour diverses tâches de carnet d’adresses, y compris l’ouverture des conteneurs de carnet d’adresses, recherche des utilisateurs de messagerie et de boîtes de dialogue affichage adresse. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

 **OpenAddressBook** peut renvoyer MAPI_W_ERRORS_RETURNED si elle ne peut pas charger une ou plusieurs des fournisseurs de carnet d’adresses dans le profil actif. Cette valeur est un avertissement et vous devez traiter l’appel comme réussie. Même si tous les fournisseurs de carnet d’adresses Échec du chargement, **OpenAddressBook** toujours réussit, renvoyant MAPI_W_ERRORS_RETURNED et un pointeur **IAddrBook** dans le paramètre _lppAdrBook_ . Étant donné que **OpenAddressBook** retourne toujours un pointeur **IAddrBook** valide, vous devez le libérer lorsque vous avez fini de l’utiliser. 
  
Impossible de charger un ou plusieurs fournisseurs de carnet d’adresses, appelez [IMAPISupport::GetLastError](imapisupport-getlasterror.md) pour obtenir une structure [MAPIERROR](mapierror.md) qui contient des informations sur les fournisseurs qui n’a pas été chargé. 
  
## <a name="see-also"></a>Voir aussi



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

