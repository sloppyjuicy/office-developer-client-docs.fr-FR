---
title: IMsgServiceAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: 7f24910a-e14e-44a1-8477-d8968130ba74
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 954dc467a0d83466b1b16a3ead5b6404d372ecab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784224"
---
# <a name="imsgserviceadminopenprofilesection"></a>IMsgServiceAdmin::OpenProfileSection

  
  
**S’applique à**: Outlook 
  
Ouvre une section du profil actuel et retourne un pointeur [IProfSect](iprofsectimapiprop.md) pour davantage d’accès. 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a>Paramètres

 _lpUID_
  
> Pointeur vers la structure [MAPIUID](mapiuid.md) qui identifie la section de profil. 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à la section de profil. Transmission NULL se traduit par un pointeur vers son interface standard retourné dans le paramètre _lppProfSect_ . L’interface standard pour une section de profil est **IProfSect**.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’accès à la section de profil. Les indicateurs suivants peuvent être définis :
    
MAPI_DEFERRED_ERRORS 
  
> Permet **OpenProfileSection** retournée correctement, éventuellement avant le profil de section est totalement disponible au client appelant. Si la section profil n’est pas disponible, vous appelez suivante pour qu’il peut déclencher une erreur. 
    
N' 
  
> Demandes d’autorisation de lecture/écriture. Par défaut, les sections de profil sont ouverts avec l’autorisation en lecture seule et clients ne doivent pas fonctionner en supposant que bénéficie des autorisations en lecture/écriture. 
    
MAPI_FORCE_ACCESS
  
> Permet d’accéder à toutes les sections de profil, y compris ceux détenus par les fournisseurs de services individuels.
    
 _lppProfSect_
  
> [out] Pointeur vers un pointeur vers la section de profil.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La section profil a été ouvert avec succès.
    
MAPI_E_NO_ACCESS 
  
> Une tentative a été effectuée pour accéder à une section de profil pour lequel l’appelant dispose d’autorisations insuffisantes.
    
MAPI_E_NOT_FOUND 
  
> La section profil demandée n’existe pas.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin::OpenProfileSection** ouvre une section de profil, un objet qui prend en charge l’interface [IProfSect](iprofsectimapiprop.md) . Les sections de profil sont utilisées pour la lecture et l’écriture d’informations sur le profil de la session. 
  
 **OpenProfileSection** ne peut pas être utilisé pour ouvrir des sections profil détenues par les fournisseurs de services individuels, sauf si MAPI_FORCE_ACCESS est utilisé. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Plusieurs clients peuvent ouvrir une section de profil avec l’autorisation en lecture seule, mais qu’un seul client peut ouvrir une section de profil avec l’autorisation de lecture/écriture. Si un autre client a une section de profil ouvrir que vous essayez d’ouvrir en appelant **OpenProfileSection** avec l’indicateur n’est défini, l’appel échoue, renvoi MAPI_E_NO_ACCESS. 
  
Une opération d’ouverture en lecture seule échoue si la section est ouverte en écriture. 
  
Vous pouvez créer une section de profil en appelant **OpenProfileSection** avec l’indicateur n’et une structure [MAPIUID](mapiuid.md) qui n’existe pas dans le paramètre _lpUID_ . N’oubliez pas que vous spécifiez ne. Si vous définissez _lpUID_ pour pointer vers un inexistante **MAPIUID** et **OpenProfileSection** est configuré pour utiliser le mode par défaut l’accès en lecture seule, l’appel échoue avec le message MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI utilise la méthode **IMsgServiceAdmin::OpenProfileSection** pour ouvrir une section de profil.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

