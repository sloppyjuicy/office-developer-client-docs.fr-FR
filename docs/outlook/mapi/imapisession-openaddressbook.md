---
title: IMAPISessionOpenAddressBook
description: IMAPISessionOpenAddressBook ouvre le carnet d’adresses intégré MAPI, en retournant un pointeur IAddrBook pour un accès supplémentaire.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.OpenAddressBook
api_type:
- COM
ms.assetid: 2b6a4c6a-bb71-4ea1-a3b6-90a2722880fb
ms.openlocfilehash: bdcfc4309350c53771ca299e61fe7ca507411dcd
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827960"
---
# <a name="imapisessionopenaddressbook"></a>IMAPISession::OpenAddressBook

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre le carnet d’adresses intégré MAPI, en retournant un pointeur [IAddrBook](iaddrbookimapiprop.md) pour un accès supplémentaire. 
  
```cpp
HRESULT OpenAddressBook(
  ULONG_PTR ulUIParam,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Handle de la fenêtre parente de la boîte de dialogue d’adresse commune et d’autres affichages associés.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au carnet d’adresses. Le passage de **la valeur null** renvoie un pointeur vers l’interface standard du carnet d’adresses, [IAddrBook : IMAPIProp](iaddrbookimapiprop.md). 
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle l’ouverture du carnet d’adresses. L’indicateur suivant peut être défini :
    
AB_NO_DIALOG 
  
> Supprime l’affichage des boîtes de dialogue. Si l’indicateur AB_NO_DIALOG n’est pas défini, les fournisseurs de carnets d’adresses qui contribuent au carnet d’adresses intégré peuvent demander à l’utilisateur les informations nécessaires. 
    
 _lppAdrBook_
  
> [out] Pointeur vers un pointeur vers le carnet d’adresses.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le carnet d’adresses a été ouvert avec succès.
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi, mais les conteneurs d’un ou plusieurs fournisseurs de carnets d’adresses n’ont pas pu être ouverts. Lorsque cet avertissement est retourné, l’appel doit être traité comme ayant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::OpenAddressBook** ouvre le carnet d’adresses intégré MAPI, une collection des conteneurs de niveau supérieur de tous les fournisseurs de carnets d’adresses dans le profil. Le pointeur retourné dans le paramètre _lppAdrBook_ fournit un accès supplémentaire au contenu du carnet d’adresses. Cela permet à l’appelant d’effectuer des tâches telles que l’ouverture de conteneurs individuels, la recherche d’utilisateurs de messagerie et l’affichage de boîtes de dialogue d’adresse communes. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

 **OpenAddressBook** retourne MAPI_W_ERRORS_RETURNED s’il ne peut pas charger un ou plusieurs fournisseurs de carnet d’adresses dans le profil. Cette valeur est un avertissement, et non une valeur d’erreur ; le gérer comme vous le feriez S_OK. **OpenAddressBook** retourne toujours un pointeur valide dans le paramètre _lppAdrBook_ , quel que soit le nombre de fournisseurs de carnets d’adresses qui n’ont pas pu être chargés. Par conséquent, vous devez toujours appeler la méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) du carnet d’adresses à un moment donné avant de vous déconnecter. 
  
Quand **OpenAddressBook** retourne MAPI_W_ERRORS_RETURNED, appelez [IMAPISession::GetLastError](imapisession-getlasterror.md) pour obtenir une structure [MAPIERROR](mapierror.md) qui contient des informations sur les fournisseurs défaillants. Une structure **MAPIERROR** unique est retournée qui contient des informations fournies par tous les fournisseurs. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::GetAddrBook  <br/> |MFCMAPI utilise la méthode **IMAPISession::OpenAddressBook** pour obtenir le carnet d’adresses intégré. |
   
## <a name="see-also"></a>Voir aussi



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::GetLastError](imapisession-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

