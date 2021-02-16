---
title: IMAPISessionOpenAddressBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenAddressBook
api_type:
- COM
ms.assetid: 2b6a4c6a-bb71-4ea1-a3b6-90a2722880fb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 51bf5f8455d4cb790d0c955e96249b0f9deef1af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329420"
---
# <a name="imapisessionopenaddressbook"></a>IMAPISession::OpenAddressBook

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre le carnet d’adresses intégré MAPI, en renvoyant un [pointeur IAddrBook](iaddrbookimapiprop.md) pour un accès supplémentaire. 
  
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
  
> [in] Poignée vers la fenêtre parente de la boîte de dialogue d’adresse commune et autres affichages associés.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au carnet d’adresses. La **transmission de la** valeur null renvoie un pointeur vers l’interface standard du carnet d’adresses, [IAddrBook : IMAPIProp](iaddrbookimapiprop.md). 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’ouverture du carnet d’adresses. L’indicateur suivant peut être définie :
    
AB_NO_DIALOG 
  
> Supprime l’affichage des boîtes de dialogue. Si l’AB_NO_DIALOG n’est pas définie, les fournisseurs de carnet d’adresses qui contribuent au carnet d’adresses intégré peuvent inviter l’utilisateur à fournir les informations nécessaires. 
    
 _lppAdrBook_
  
> [out] Pointeur vers un pointeur vers le carnet d’adresses.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le carnet d’adresses a été ouvert avec succès.
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi, mais les conteneurs d’un ou plusieurs fournisseurs de carnet d’adresses n’ont pas pu être ouverts. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED.** Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISession::OpenAddressBook** ouvre le carnet d’adresses intégré MAPI, une collection des conteneurs de niveau supérieur de tous les fournisseurs de carnet d’adresses du profil. Le pointeur renvoyé dans le  _paramètre lppAdrBook_ fournit un accès supplémentaire au contenu du carnet d’adresses. Cela permet à l’appelant d’effectuer des tâches telles que l’ouverture de conteneurs individuels, la recherche d’utilisateurs de messagerie et l’affichage de boîtes de dialogue d’adresse communes. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

 **OpenAddressBook renvoie** MAPI_W_ERRORS_RETURNED si elle ne peut pas charger un ou plusieurs des fournisseurs de carnet d’adresses dans le profil. Cette valeur est un avertissement, et non une valeur d’erreur . gérer comme vous le feriez S_OK. **OpenAddressBook renvoie** toujours un pointeur valide dans le paramètre  _lppAdrBook,_ quel que soit le nombre de fournisseurs de carnet d’adresses dont le chargement a échoué. Par conséquent, vous devez toujours appeler la méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) du carnet d’adresses à un moment donné avant de vous dé connecter. 
  
Lorsque **OpenAddressBook** renvoie MAPI_W_ERRORS_RETURNED, appelez [IMAPISession::GetLastError](imapisession-getlasterror.md) pour obtenir une structure [MAPIERROR](mapierror.md) qui contient des informations sur les fournisseurs défaillants. Une structure **MAPIERROR** unique qui contient les informations fournies par tous les fournisseurs est renvoyée. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::GetAddrBook  <br/> |MFCMAPI utilise la **méthode IMAPISession::OpenAddressBook** pour obtenir le carnet d’adresses intégré.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::GetLastError](imapisession-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

