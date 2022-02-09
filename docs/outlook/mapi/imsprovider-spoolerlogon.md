---
title: IMSProviderSpoolerLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSProvider.SpoolerLogon
api_type:
- COM
ms.assetid: 79d5af23-efad-4013-a330-56babfb2bb0f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3a7640f0591157b40cf552705d02d613a8ebad92
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62461502"
---
# <a name="imsproviderspoolerlogon"></a>IMSProvider::SpoolerLogon

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Connecte lepooler MAPI à une magasin de messages.
  
```cpp
HRESULT SpoolerLogon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  LPCIID lpInterface,
  ULONG cbSpoolSecurity,
  LPBYTE lpbSpoolSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPMSLOGON FAR * lppMSLogon,
  LPMDB FAR * lppMDB     
);
```

## <a name="parameters"></a>Paramètres

 _lpMAPISup_
  
> [in] Pointeur vers l’objet de support MAPI pour la magasin de messages.
    
 _ulUIParam_
  
> [in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode. 
    
 _lpszProfileName_
  
> [in] Pointeur vers une chaîne qui contient le nom du profil utilisé pour la logo dupooler MAPI. Cette chaîne peut être affichée dans des boîtes de dialogue, écrite dans un fichier journal ou simplement ignorée. Elle doit être au format Unicode si l’MAPI_UNICODE est définie dans _le paramètre ulFlags_ . 
    
 _cbEntryID_
  
> [in] Taille, en octets, de l’identificateur d’entrée pointé par  _le paramètre lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée de la boutique de messages. La transmission de la valeur NULL dans le paramètre _lpEntryID_ indique qu’une magasin de messages n’a pas encore été sélectionnée et que les boîtes de dialogue qui permettent à l’utilisateur de sélectionner une magasin de messages peuvent être présentées. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’utilisation de l’logo. Les indicateurs suivants peuvent être définies :
    
MAPI_DEFERRED_ERRORS 
  
> L’appel est autorisé à réussir même si l’objet sous-jacent n’est pas disponible pour l’implémentation de l’appelant. Si l’objet n’est pas disponible, un appel ultérieur à l’objet peut occasioner une erreur.
    
MAPI_UNICODE 
  
> Les chaînes transmises sont au format Unicode. Si MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
MDB_NO_DIALOG 
  
> Empêche l’affichage des boîtes de dialogue d’affichage. Si cet indicateur est définie, la valeur d’MAPI_E_LOGON_FAILED’erreur est renvoyée si l’échec de la logon. Si cet indicateur n’est pas définie, le fournisseur de la boutique de messages peut inviter l’utilisateur à corriger un nom ou un mot de passe, à insérer un disque ou à effectuer d’autres actions nécessaires pour établir une connexion à la boutique.
    
MDB_WRITE 
  
> Demande une autorisation de lecture/écriture.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) de connexion à la boutique de messages. La transmission de la valeur NULL indique que l’interface MAPI pour la magasin de messages ([IMsgStore](imsgstoreimapiprop.md)) est renvoyée. Le  _paramètre lpInterface_ peut également être définie sur un identificateur pour une interface appropriée pour la magasin de messages (par exemple, IID_IUnknown ou IID_IMAPIProp). 
    
 _cbSpoolSecurity_
  
> [in] Pointeur vers la taille, en octets, des données de validation dans _le paramètre lppbSpoolSecurity_ . 
    
 _lpbSpoolSecurity_
  
> [in] Pointeur vers un pointeur vers des données de validation. La méthode **SpoolerLogon** utilise ces données pour connecter lepooler MAPI à la même boutique que le fournisseur de magasins de messages précédemment connecté à l’aide de la méthode [IMSProvider::Logon](imsprovider-logon.md) . 
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers la structure [MAPIERROR](mapierror.md) renvoyée, le caser, qui contient des informations de version, de composant et de contexte pour une erreur. Le  _paramètre lppMAPIError_ peut avoir la valeur NULL s’il n’existe aucune structure **MAPIERROR** à renvoyer. 
    
 _lppMSLogon_
  
> [out] Pointeur vers le pointeur vers l’objet d’ouverture de session de la boutique de messages pour que MAPI se connecte.
    
 _lppMDB_
  
> [out] Pointeur vers le pointeur vers l’objet de magasin de messages pour lepooler MAPI et les applications clientes à connecter.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_UNCONFIGURED 
  
> Le profil ne contient pas suffisamment d’informations pour que la logon soit terminée. Lorsque cette valeur est renvoyée, MAPI appelle la fonction de point d’entrée du service de messagerie du fournisseur de messages.
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi, mais des informations d’erreur sont disponibles pour le fournisseur de la boutique de messages. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED’avertissement** . Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md). Pour obtenir les informations d’erreur du fournisseur, appelez la méthode [IMAPISession::GetLastError](imapisession-getlasterror.md) . 
    
## <a name="remarks"></a>Remarques

Lepooler MAPI appelle la méthode **IMSProvider::SpoolerLogon** pour se connecter à une magasin de messages. Lepooler MAPI doit utiliser l’objet de banque de messages renvoyé par le fournisseur de banque de messages dans le paramètre _lppMDB_ pendant et après l’ouverture de connecté. 
  
Pour des raisons de cohérence avec la méthode [IMSProvider::Logon](imsprovider-logon.md) , le fournisseur renvoie également un objet d’ouverture de messagerie dans le paramètre _lppMSLogon_ . L’utilisation de l’objet store et de l’objet d’ouverture de connecté sont identiques pour l’ouverture de magasin habituelle ; il doit y avoir une correspondance un-à-un entre l’objet d’ouverture de ligne et l’objet store afin que les objets agissent comme s’il s’agit d’un objet qui expose deux interfaces. Les deux objets sont créés ensemble et libérés ensemble. 
  
Le fournisseur de magasin doit marquer en interne l’objet de magasin de messages renvoyé pour indiquer que la boutique est utilisée par lepooler MAPI. Certaines méthodes de cet objet store se comportent différemment de l’objet de magasin de messages fourni aux applications clientes. Conserver cette marque interne est le moyen le plus courant de déclencher le comportement spécifique aupooler MAPI.
  
## <a name="see-also"></a>Voir aussi



[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIERROR](mapierror.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

