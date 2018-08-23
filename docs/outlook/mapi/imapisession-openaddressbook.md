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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 0902aeb71ed66381772a808d21d77edb7e0e2da8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589874"
---
# <a name="imapisessionopenaddressbook"></a>IMAPISession::OpenAddressBook

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Ouvre le carnet d’adresses intégré MAPI, qui retourne un pointeur [IAddrBook](iaddrbookimapiprop.md) pour davantage d’accès. 
  
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
  
> [in] Un handle vers la fenêtre parent de la boîte de dialogue commune adresse et d’autres liées affiche.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au carnet d’adresses. Interface standard du carnet d’adresses, en passant **null** renvoie un pointeur [IAddrBook : IMAPIProp](iaddrbookimapiprop.md). 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’ouverture du carnet d’adresses. Vous pouvez définir l’indicateur suivant :
    
AB_NO_DIALOG 
  
> Supprime l’affichage des boîtes de dialogue. Si l’indicateur AB_NO_DIALOG n’est pas définie, les fournisseurs de carnet d’adresses qui contribuent au carnet d’adresses intégré peuvent inviter l’utilisateur à toutes les informations nécessaires. 
    
 _lppAdrBook_
  
> [out] Pointeur vers un pointeur vers le carnet d’adresses.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le carnet d’adresses a été ouvert avec succès.
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi, mais les conteneurs d’un ou plusieurs fournisseurs de carnet d’adresses n’a pas peuvent être ouvert. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::OpenAddressBook** ouvre le carnet d’adresses intégré MAPI, une collection des conteneurs de tous les fournisseurs de carnet d’adresses dans le profil de niveau supérieur. Le pointeur est retourné dans le paramètre _lppAdrBook_ fournit davantage l’accès au contenu du carnet d’adresses. Cela permet à l’appelant effectuer des tâches telles que l’ouverture des conteneurs individuels, recherche des utilisateurs de messagerie et l’affichage des boîtes de dialogue communes adresse. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

 **OpenAddressBook** renvoie MAPI_W_ERRORS_RETURNED si elle ne peut pas charger une ou plusieurs des fournisseurs de carnet d’adresses dans le profil. Cette valeur est un message d’avertissement, pas une valeur d’erreur ; gérer comme vous le feriez S_OK. **OpenAddressBook** renvoie toujours un pointeur valide dans le paramètre _lppAdrBook_ , quel que soit le nombre des fournisseurs de carnet d’adresses n’a pas pu charger. Par conséquent, vous devez toujours appeler méthode de [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) du carnet d’adresses à un moment donné avant la fermeture de session. 
  
Lorsque **OpenAddressBook** renvoie MAPI_W_ERRORS_RETURNED, appelez [IMAPISession::GetLastError](imapisession-getlasterror.md) pour obtenir une structure [MAPIERROR](mapierror.md) qui contient des informations sur les fournisseurs défectueux. Une structure **MAPIERROR** unique est retournée qui contient les informations fournies par tous les fournisseurs. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::GetAddrBook  <br/> |MFCMAPI utilise la méthode **IMAPISession::OpenAddressBook** pour obtenir le carnet d’adresses intégré.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::GetLastError](imapisession-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

