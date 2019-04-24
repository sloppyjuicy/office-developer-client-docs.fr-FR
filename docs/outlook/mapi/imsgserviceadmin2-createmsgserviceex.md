---
title: IMsgServiceAdmin2CreateMsgServiceEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin2.CreateMsgServiceEx
api_type:
- COM
ms.assetid: 4910dabd-9380-4fde-a440-5c64d74c0bba
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: b7fe25491228f00f6865af963db36f27bae5d7a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310009"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a>IMsgServiceAdmin2::CreateMsgServiceEx

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajoute un service de messagerie au profil actif et renvoie cet UID de service nouvellement ajouté.
  
```cpp
HRESULT CreateMsgServiceEx(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,    
  LPMAPIUID lpuidService
);
```

## <a name="parameters"></a>Paramètres

 _lpszService_
  
> dans Pointeur vers le nom du service de messagerie à ajouter. Ce nom de service de message doit apparaître dans la section **[services]** du fichier MapiSvc. inf. 
    
 _lpszDisplayName_
  
> dans Pointeur vers le nom d'affichage du service de messagerie à ajouter. Le paramètre _lpszDisplayName_ est ignoré si le service de messagerie a défini la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) dans le fichier MapiSvc. inf.
    
 _ulUIParam_
  
> dans Handle de la fenêtre parente de toutes les boîtes de dialogue ou fenêtres que cette méthode affiche.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le mode d'installation du service de messagerie. Les indicateurs suivants peuvent être définis:
    
MAPI_UNICODE
  
> Les paramètres lpszService et lpszDisplayName doivent être castés en LPWSTR et interprétés comme des chaînes Unicode.
    
SERVICE_NO_RESTART_WARNING
  
> Lors de l'ajout d'un nouveau service de messagerie au profil, le sous-système MAPI, basé sur différentes circonstances et critères, détermine souvent que cette action nécessite un redémarrage d'Outlook. Si l'indicateur SERVICE_NO_RESTART_WARNING n'est pas inclus et que l'interface utilisateur est autorisée (en fonction des indicateurs SERVICE_UI_ALWAYS et SERVICE_UI_ALLOWED) et qu'au moins un processus est connecté au profil actuel, cette fonction affiche le message «vous devez redémarrer Outlook pour Ces modifications prennent effet. " L'ajout de l'indicateur SERVICE_NO_RESTART_WARNING supprime l'affichage de ce message d'avertissement.
    
SERVICE_UI_ALLOWED
  
> L'interface utilisateur de configuration du service de messagerie est autorisée si nécessaire.
    
SERVICE_UI_ALWAYS
  
> Le service de messagerie affiche sa feuille de propriétés de configuration.
    
 _lpuidService_
  
> remarquer Pointeur vers l'UID du service de messagerie ajouté.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NOT_FOUND
  
> Le nom du service de messagerie ne figure pas dans la section **[services]** du fichier MapiSvc. inf. 
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin2:: CreateMsgServiceEx** ajoute un service de messagerie au profil actif. **CreateMsgServiceEx** appelle la fonction de point d'entrée du service de messagerie pour effectuer les tâches de configuration propres au service. Si l'indicateur SERVICE_UI_ALLOWED est défini dans le paramètre _ulFlags_ , le service de messagerie en cours d'installation peut afficher une feuille de propriétés permettant à l'utilisateur de configurer ses paramètres. 
  
Le fichier MapiSvc. INF contient la liste des fournisseurs qui composent un service de messagerie et les propriétés de chacune d'elles. **CreateMsgServiceEx** crée d'abord une section de profil pour le service de messagerie, puis copie toutes les informations pour ce service à partir du fichier MapiSvc. inf dans le profil, créant de nouvelles sections pour chaque fournisseur. 
  
Une fois que toutes les informations ont été copiées à partir de MapiSvc. inf, la fonction de point d'entrée du service de messagerie, **MSGSERVICEENTRY**, est appelée avec la valeur MSG_SERVICE_CREATE définie dans le paramètre _ulContext_ . Si l'indicateur SERVICE_UI_ALLOWED est défini dans le paramètre _ulFlags_ de la méthode **CreateMsgServiceEx** , les valeurs des paramètres _ulUIParam_ et _ulFlags_ sont également transmises lors de l'appel à la fonction point d'entrée du service de messagerie. Les fournisseurs de services doivent afficher leurs feuilles de propriétés de configuration afin que les utilisateurs puissent configurer le service de messagerie. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si l'argument **CreateMsgServiceEx** _lpuidService_ n'a pas la valeur null, la propriété **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) du service de messagerie qui a été ajouté au profil est renvoyée dans le **GUID** vers lequel il pointe. 
  
TransMettez la valeur de la propriété **PR_SERVICE_UID** dans le paramètre _lpuidService_ à la méthode [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) pour configurer le service. 
  
> [!CAUTION]
> L'implémentation Microsoft Outlook 2010 du sous-système MAPI ne prend pas en charge MAPI_UNICODE et échoue si elle est utilisée. 
  
> [!IMPORTANT]
> L'interface IMsgServiceAdmin2 est exposée par le même objet qui implémente l'interface IMsgServiceAdmin et est disponible à l'aide de l'implémentation Outlook du sous-système MAPI depuis Outlook 2003. Son IID est défini comme suit: > `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> le _ulFlags_ SERVICE_NO_RESTART_WARNING n'est peut-être pas défini dans le fichier d'en-tête téléchargeable dont vous disposez actuellement, auquel cas vous pouvez l'ajouter à votre code à l'aide de la valeur suivante: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin2 : IMsgServiceAdmin](imsgserviceadmin2imsgserviceadmin.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

