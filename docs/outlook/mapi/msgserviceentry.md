---
title: MSGSERVICEENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MSGSERVICEENTRY
api_type:
- COM
ms.assetid: 655774a6-588c-44c7-903b-4497b7eccbc2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 56a5f153dbd563397b9216af32a715692d0876d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427877"
---
# <a name="msgserviceentry"></a>MSGSERVICEENTRY

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit un prototype pour une fonction de point d'entrée de service de message permettant de prendre en charge la configuration du service de messagerie. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi. h  <br/> |
|Fonction définie implémentée par:  <br/> |Services de messagerie  <br/> |
|Fonction définie appelée par:  <br/> |MAPI  <br/> |
   
```cpp
HRESULT MSGSERVICEENTRY(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulContext,
  ULONG cValues,
  LPSPropValue lpProps,
  LPPROVIDERADMIN lpProviderAdmin,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a>Paramètres

 _hInstance_
  
> dans Handle de l'instance du service providerDLL. Le descripteur est généralement utilisé pour récupérer des ressources. 
    
 _lpMalloc_
  
> dans Pointeur vers un objet de l'allocation de mémoire qui expose **** l'interface OLE imalloc. Le service de messagerie peut avoir besoin d'utiliser cette méthode d'allocation lorsque vous travaillez avec certaines interfaces telles que **IStream**. 
    
 _lpMAPISup_
  
> dans Pointeur vers une implémentation d'interface [IUnknown IMAPISupport:](imapisupportiunknown.md) . 
    
 _ulUIParam_
  
> dans Valeur propre à l'implémentation utilisée pour passer des informations d'interface utilisateur à une fonction ou à zéro. Le paramètre _ulUIParam_ est le descripteur de fenêtre parent de la boîte de dialogue de configuration et est de type HWND (Cast à a ULONG_PTR). La valeur zéro indique qu'il n'y a aucune fenêtre parente. 
    
 _ulFlags_
  
> dans Masque de réindicateur des indicateurs indiquant les options de la fonction d'entrée de service. Les indicateurs suivants peuvent être définis:
    
MAPI_UNICODE 
  
> Les chaînes transmises sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI. 
    
MSG_SERVICE_UI_READ_ONLY 
  
> L'interface utilisateur de configuration du service doit afficher la configuration actuelle, mais pas autoriser l'utilisateur à la modifier. 
    
SERVICE_UI_ALLOWED 
  
> Permet l'affichage d'une boîte de dialogue de configuration si nécessaire. Lorsque l'indicateur SERVICE_UI_ALLOWED est défini, la boîte de dialogue ne doit être affichée que si le tableau de valeurs de la propriété _lpProps_ est vide ou ne contient pas une configuration valide. Si SERVICE_UI_ALLOWED n'est pas défini, une boîte de dialogue peut toujours s'afficher si l'indicateur SERVICE_UI_ALWAYS est défini. 
    
UI_CURRENT_PROVIDER_FIRST 
  
> Demande que la boîte de dialogue de configuration pour le fournisseur actif s'affiche en haut des autres boîtes de dialogue. 
    
SERVICE_UI_ALWAYS 
  
> Le service de messagerie doit afficher une boîte de dialogue de configuration. Si l'indicateur SERVICE_UI_ALWAYS n'est pas défini, une boîte de dialogue de configuration peut toujours s'afficher si l'indicateur SERVICE_UI_ALLOWED est défini et si des informations de configuration valides ne sont pas disponibles à partir du tableau de valeurs de la propriété _lpProps_ . SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS doit être défini pour permettre l'affichage de l'interface utilisateur. 
    
 _ulContext_
  
> dans Opération de configuration que MAPI effectue actuellement. Le paramètre _ulContext_ contient l'une des valeurs suivantes: 
    
MSG_SERVICE_CONFIGURE 
  
> Les modifications apportées à la configuration du service doivent être effectuées dans le profil. Si l'indicateur SERVICE_UI_ALWAYS est défini, le service doit afficher sa boîte de dialogue de configuration. La boîte de dialogue doit également être affichée si l'indicateur SERVICE_UI_ALLOWED est défini et si le paramètre _lpProps_ est vide ou ne contient pas de données de configuration valides. Si _lpProps_ contient des données valides, aucune boîte de dialogue ne doit s'afficher et le service doit utiliser ces données pour procéder à la modification de la configuration. 
    
MSG_SERVICE_CREATE 
  
> Le service est ajouté à un profil. Si l'indicateur SERVICE_UI_ALWAYS ou SERVICE_UI_ALLOWED est défini, le service doit afficher sa boîte de dialogue de configuration. Si aucun indicateur n'est défini, le service doit échouer. 
    
MSG_SERVICE_DELETE 
  
> Le service est en cours de suppression d'un profil. Après réception de cet événement, le service doit retourner S_OK.
    
MSG_SERVICE_INSTALL 
  
> Le service a été installé sur la station de travail de l'utilisateur à partir d'un réseau, d'une disquette ou d'un autre support externe. Après réception de cet événement, le service renvoie généralement S_OK. 
    
MSG_SERVICE_PROVIDER_CREATE 
  
> Demande que le service crée une instance supplémentaire d'un fournisseur. Si le service prend en charge cette opération, il doit appeler [IProviderAdmin:: CreateProvider](iprovideradmin-createprovider.md). Si le service ne prend pas en charge cette opération, il peut renvoyer MAPI_E_NO_SUPPORT. 
    
MSG_SERVICE_PROVIDER_DELETE 
  
> Demande que le service supprime une instance de fournisseur. Si le service prend en charge cette opération, il doit appeler [IProviderAdmin::D eleteprovider](iprovideradmin-deleteprovider.md). Si le service ne prend pas en charge cette opération, il peut renvoyer MAPI_E_NO_SUPPORT.
    
MSG_SERVICE_UNINSTALL 
  
> Le service est en cours de suppression. Après avoir reçu cet événement, le service peut effectuer toutes les tâches de nettoyage qui doivent être effectuées avant la fin du service, puis renvoyer avec une valeur de réussite. Si l'utilisateur annule la suppression, le service doit renvoyer MAPI_E_USER_CANCEL. 
    
 _cValues_
  
> dans Nombre de valeurs de propriété dans le tableau vers lequel pointe le paramètre _lpProps_ . La valeur du paramètre _cValues_ est égale à zéro si MAPI ne transmet aucune valeur de propriété. 
    
 _lpProps_
  
> dans Pointeur vers un tableau facultatif de structures [SPropValue](spropvalue.md) indiquant des valeurs pour les propriétés prises en charge par le fournisseur que la fonction utilisera lors de la configuration du service de messagerie. La fonction utilise ce paramètre uniquement si le paramètre _ulContext_ est défini sur MSG_SERVICE_CONFIGURE. Ce paramètre est couramment utilisé pour transmettre le chemin d'accès à un fichier pour un service basé sur des fichiers, tel qu'un service de carnet d'adresses personnel. Si l'indicateur MSG_SERVICE_CONFIGURE n'est pas passé dans le paramètre _ulFlags_ , le paramètre _lpProps_ doit être égal à zéro. 
    
 _lpProviderAdmin_
  
> dans Pointeur vers une interface [IProviderAdmin: IUnknown](iprovideradminiunknown.md) que la fonction peut utiliser pour localiser les sections de profil d'un fournisseur spécifique dans le service de messagerie actuel. 
    
 _lppMapiError_
  
> remarquer Pointeur vers une structure [MAPIERROR](mapierror.md) . La structure est allouée à l'aide de la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) . Tous les membres sont facultatifs, bien que la plupart des structures contiennent une chaîne de message d'erreur valide dans le membre _lpszError_ . Si les membres _lpszComponent_ ou _lpszError_ de la structure sont présents, leur mémoire doit éventuellement être libérée par un seul appel à [MAPIFreeBuffer](mapifreebuffer.md) sur la structure de base. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_UNCONFIGURED 
  
> Le fournisseur de services n'a pas été configuré. 
    
MAPI_E_USER_CANCEL 
  
> L'utilisateur a annulé l'opération, généralement en cliquant sur le bouton **Annuler** d'une boîte de dialogue. 
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur ne prend pas en charge les modifications apportées à ses objets ou ne prend pas en charge la notification des modifications. 
    
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et l'implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et l'implémentation prend en charge uniquement Unicode.
    
## <a name="remarks"></a>Remarques

Une fonction définie à l'aide du prototype de fonction **MSGSERVICEENTRY** permet aux services de messagerie de se configurer eux-mêmes ou d'effectuer d'autres actions de service spécifiques. La fonction fournit principalement une boîte de dialogue dans laquelle l'utilisateur peut modifier les paramètres propres au service de messagerie. Il peut également prendre en charge la configuration par programme à l'aide du tableau de valeurs de propriété passé dans le paramètre _lpProps_ . La configuration par programme est facultative à moins que le service ne prenne en charge l'Assistant Profil, pour lequel il est requis. 
  
MAPI appelle ce point d'entrée à partir de l'application du panneau de configuration ou en réponse à une application cliente qui appelle [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) ou [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
MAPI ne place aucune restriction sur le nom de la fonction qu'un service de messagerie utilise pour le prototype **MSGSERVICEENTRY** mais préfère le nom **ServiceEntry**. Il n'existe aucune restriction quant à l'ordinal de la fonction, et une seule DLL de fournisseur peut contenir plusieurs fonctions. Toutefois, une seule des fonctions peut être nommée **ServiceEntry**. 
  
Un service de messagerie peut utiliser la fonction [BuildDisplayTable](builddisplaytable.md) et la méthode [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) pour simplifier l'implémentation de la boîte de dialogue de configuration. 
  
Un utilisateur peut annuler une opération MSG_SERVICE_UNINSTALL. Dans ce cas, la fonction **ServiceEntry** doit vérifier auprès de l'utilisateur que le service ne doit pas être supprimé et renvoyer MAPI_E_USER_CANCEL si le service reste installé. 
  
Une fonction basée sur le prototype **MSGSERVICEENTRY** renvoie l'une des valeurs HRESULT indiquées. MAPI transfère cette valeur lors de la réponse à l'appel d'un client à [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
Les services de messagerie qui exportent une fonction d'entrée de service doivent inclure les propriétés **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) et **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) dans la section service de messagerie de MAPISVC. INF. 
  

