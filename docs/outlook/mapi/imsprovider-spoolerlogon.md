---
title: IMSProviderSpoolerLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.SpoolerLogon
api_type:
- COM
ms.assetid: 79d5af23-efad-4013-a330-56babfb2bb0f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 56c025713b0cc2b41a4bf4463f48f8d7c3d2124b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586416"
---
# <a name="imsproviderspoolerlogon"></a>IMSProvider::SpoolerLogon

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Enregistre le spouleur MAPI sur une banque de messages.
  
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
  
> [in] Un pointeur vers l’interface MAPI prennent en charge l’objet de la banque de messages.
    
 _ulUIParam_
  
> [in] Un handle vers la fenêtre parent des boîtes de dialogue ni windows cette méthode affiche. 
    
 _lpszProfileName_
  
> [in] Pointeur vers une chaîne qui contient le nom du profil utilisé pour l’ouverture de session MAPI spouleur. Cette chaîne peut être affichée dans les boîtes de dialogue, écrite dans un fichier journal ou ignorée. Si l’indicateur MAPI_UNICODE est défini dans le paramètre _ulFlags_ , elle doit être au format Unicode. 
    
 _cbEntryID_
  
> [in] La taille, en octets, de l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée de la banque de messages. Passage de NULL dans le paramètre _lpEntryID_ indique qu’une banque de messages n’a pas encore été sélectionnée et que les boîtes de dialogue permettant à l’utilisateur de sélectionner une banque de messages peuvent être présentées. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont les paramètres de connexion est effectuée. Les indicateurs suivants peuvent être définis :
    
MAPI_DEFERRED_ERRORS 
  
> L’appel est autorisé à fonctionne même si l’objet sous-jacent n’est pas disponible pour l’implémentation d’appel. Si l’objet n’est pas disponible, un appel à l’objet suivant peut déclencher une erreur.
    
MAPI_UNICODE 
  
> Les chaînes passée sont au format Unicode. Si MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
MDB_NO_DIALOG 
  
> Empêche l’affichage des boîtes de dialogue d’ouverture de session. Si cet indicateur est défini, la valeur d’erreur MAPI_E_LOGON_FAILED est renvoyée si l’ouverture de session échoue. Si cet indicateur n’est pas défini, le fournisseur de banque de message peut inviter l’utilisateur à corriger un nom ou le mot de passe, à insérer un disque ou à effectuer d’autres actions nécessaires pour établir une connexion à la base.
    
MDB_WRITE 
  
> Demandes d’autorisation de lecture/écriture.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) pour la banque de messages pour vous connecter à. Valeur null indique l’interface MAPI pour la banque de messages ([IMsgStore](imsgstoreimapiprop.md)) est renvoyée. Le paramètre _lpInterface_ peut également être défini à un identificateur pour une interface appropriée pour la banque de messages (par exemple IID_IUnknown ou IID_IMAPIProp). 
    
 _cbSpoolSecurity_
  
> [in] Pointeur vers la taille, en octets, des données de validation dans le paramètre _lppbSpoolSecurity_ . 
    
 _lpbSpoolSecurity_
  
> [in] Pointeur vers un pointeur vers les données de validation. La méthode **SpoolerLogon** utilise ces données pour ouvrir une session en tant que le fournisseur de banque de messages précédemment connecté à l’aide de la méthode [IMSProvider::Logon](imsprovider-logon.md) le spouleur MAPI sur le même magasin. 
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers la [MAPIERROR](mapierror.md) structure retournée, le cas échéant, qui contient des informations de version, composant et le contexte d’une erreur. Le paramètre _lppMAPIError_ peut être défini sur la valeur NULL s’il n’existe aucune structure **MAPIERROR** pour renvoyer. 
    
 _lppMSLogon_
  
> [out] Un pointeur vers le pointeur vers le message stocker l’objet d’ouverture de session MAPI pour vous connecter à.
    
 _lppMDB_
  
> [out] Un pointeur vers le pointeur vers le message stocker d’objet pour les applications clientes pour vous connecter à spouleur MAPI.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_UNCONFIGURED 
  
> Le profil ne contient pas de suffisamment d’informations pour l’ouverture de session Terminer. Lorsque cette valeur est renvoyée, MAPI appelle la fonction de point d’entrée du service de message du fournisseur de banque de messages.
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi, mais le fournisseur de banque de messages a des informations d’erreur disponibles. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md). Pour obtenir les informations d’erreur à partir du fournisseur, appelez la méthode [IMAPISession::GetLastError](imapisession-getlasterror.md) . 
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle la méthode **IMSProvider::SpoolerLogon** pour vous connecter à une banque de messages. Le spouleur MAPI doit utiliser l’objet de banque de messages renvoyé par le fournisseur de banque de messages dans le paramètre _lppMDB_ pendant et après l’ouverture de session. 
  
Pour des raisons de cohérence avec la méthode [IMSProvider::Logon](imsprovider-logon.md) , le fournisseur renvoie également un objet d’ouverture de session du magasin de message dans le paramètre _lppMSLogon_ . L’utilisation de l’objet de magasin et l’objet d’ouverture de session sont identiques pour la banque habituelles d’ouverture de session ; une correspondance entre l’objet d’ouverture de session et l’objet de magasin doit être tels que les objets se comportent comme s’ils étaient un seul objet qui expose les deux interfaces. Les deux objets sont créés, ensemble et libérés ensemble. 
  
Le fournisseur de banque doit marquer en interne de l’objet de banque de message renvoyé pour indiquer que le magasin est utilisé par le spouleur MAPI. Certaines des méthodes pour cet objet store se comportent différemment que pour le message magasin objet fourni aux applications clientes. Cette marque interne est la méthode la plus courante de déclencher le comportement spécifique pour le spouleur MAPI.
  
## <a name="see-also"></a>Voir aussi



[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIERROR](mapierror.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

