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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b7fe25491228f00f6865af963db36f27bae5d7a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410181"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a>IMsgServiceAdmin2::CreateMsgServiceEx

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajoute un service de message au profil actuel et renvoie l’UID du service nouvellement ajouté.
  
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
  
> [in] Pointeur vers le nom du service de message à ajouter. Ce nom de service de message doit apparaître dans la section **[Services]** du fichier MapiSvc.inf. 
    
 _lpszDisplayName_
  
> [in] Pointeur vers le nom complet du service de message à ajouter. Le  _paramètre lpszDisplayName_ est ignoré si le service de message a définie la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) dans le fichier MapiSvc.inf.
    
 _ulUIParam_
  
> [in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le service de message est installé. Les indicateurs suivants peuvent être définies :
    
MAPI_UNICODE
  
> Les paramètres lpszService et lpszDisplayName doivent être casté vers LPWSTR et interprétés comme des chaînes Unicode.
    
SERVICE_NO_RESTART_WARNING
  
> Lors de l’ajout d’un nouveau service de message au profil, le sous-système MAPI, en fonction de diverses circonstances et critères, détermine souvent que cette action nécessite un redémarrage d’Outlook. Si l’indicateur SERVICE_NO_RESTART_WARNING n’est pas inclus et que l’interface utilisateur est autorisée (en fonction des indicateurs SERVICE_UI_ALWAYS et SERVICE_UI_ALLOWED) et qu’au moins un processus est connecté au profil actuel, cette fonction affiche le message « Vous devez redémarrer Outlook pour que ces modifications prennent effet ». L’SERVICE_NO_RESTART_WARNING’indicateur supprime l’affichage de ce message d’avertissement.
    
SERVICE_UI_ALLOWED
  
> L’interface utilisateur de configuration du service de message est autorisée si nécessaire.
    
SERVICE_UI_ALWAYS
  
> Le service de message affiche sa feuille de propriétés de configuration.
    
 _lpuidService_
  
> [out] Pointeur vers l’UID du service de message ajouté.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NOT_FOUND
  
> Le nom du service de message ne se trouve pas dans la section **[Services]** de MapiSvc.inf. 
    
## <a name="remarks"></a>Remarques

La **méthode IMsgServiceAdmin2::CreateMsgServiceEx** ajoute un service de message au profil actuel. **CreateMsgServiceEx** appelle la fonction de point d’entrée du service de message pour effectuer des tâches de configuration spécifiques au service. Si l SERVICE_UI_ALLOWED est définie dans le paramètre  _ulFlags,_ le service de message en cours d’installation peut afficher une feuille de propriétés permettant à l’utilisateur de configurer ses paramètres. 
  
Le fichier MapiSvc.inf contient la liste des fournisseurs qui font un service de messagerie et les propriétés de chacun d’eux. **CreateMsgServiceEx** crée d’abord une section de profil pour le service de message, puis copie toutes les informations de ce service à partir du fichier MapiSvc.inf dans le profil, créant ainsi de nouvelles sections pour chaque fournisseur. 
  
Une fois toutes les informations copiées à partir de MapiSvc.inf, la fonction de point d’entrée du service de message, **MSGSERVICEENTRY**, est appelée avec la valeur MSG_SERVICE_CREATE définie dans le paramètre _ulContext._ Si l’indicateur SERVICE_UI_ALLOWED est définie dans le paramètre _ulFlags_ de la méthode **CreateMsgServiceEx,** les valeurs des paramètres _ulUIParam_ et _ulFlags_ sont également transmises lorsque la fonction de point d’entrée du service de message est appelée. Les fournisseurs de services doivent afficher leurs feuilles de propriétés de configuration afin que les utilisateurs peuvent configurer le service de messagerie. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si l’argument **CreateMsgServiceEx** _lpuidService_ n’est pas NULL, la propriété **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) du service de message qui a été ajouté au profil est renvoyée dans le **GUID** vers lequel elle pointe. 
  
Passez la valeur de la **propriété PR_SERVICE_UID** dans le paramètre  _lpuidService_ à la méthode [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) pour configurer le service. 
  
> [!CAUTION]
> L’implémentation Microsoft Outlook 2010 du sous-système MAPI ne prend pas en charge MAPI_UNICODE et échouera si elle est utilisée. 
  
> [!IMPORTANT]
> L’interface IMsgServiceAdmin2 est exposée par le même objet qui implémente l’interface IMsgServiceAdmin et est disponible à l’aide de l’implémentation d’Outlook du sous-système MAPI depuis Outlook 2003. Son IID est défini comme suit : >> Le `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);` SERVICE_NO_RESTART_WARNING _ulFlags_ peut ne pas être défini dans le fichier d’en-tête téléchargeable dont vous disposez, auquel cas vous pouvez l’ajouter à votre code à l’aide de la valeur suivante : >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="see-also"></a>Voir aussi



[IMsgServiceAdmin2 : IMsgServiceAdmin](imsgserviceadmin2imsgserviceadmin.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

