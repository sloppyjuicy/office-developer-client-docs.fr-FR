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
  
Définit un prototype pour une fonction de point d’entrée de service de message pour prendre en charge la configuration du service de message. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Fonction définie implémentée par :  <br/> |Services de messages  <br/> |
|Fonction définie appelée par :  <br/> |MAPI  <br/> |
   
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
  
> [in] Gérer l’instance de la DLL de fournisseur de services. Le handle est généralement utilisé pour récupérer des ressources. 
    
 _lpMalloc_
  
> [in] Pointeur vers un objet d’allocation de mémoire exposant l’interface OLE **IMalloc.** Le service de message peut avoir besoin d’utiliser cette méthode d’allocation lors de l’utilisation de certaines interfaces telles que **IStream**. 
    
 _lpMAPISup_
  
> [in] Pointeur vers une [implémentation d’interface IMAPISupport : IUnknown.](imapisupportiunknown.md) 
    
 _ulUIParam_
  
> [in] Valeur spécifique à l’implémentation utilisée pour transmettre des informations d’interface utilisateur à une fonction ou zéro. Le  _paramètre ulUIParam_ est le handle de fenêtre parent de la boîte de dialogue de configuration et est de type HWND (cast en ULONG_PTR). La valeur zéro indique qu’il n’y a pas de fenêtre parente. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs indiquant les options de la fonction d’entrée de service. Les indicateurs suivants peuvent être définies :
    
MAPI_UNICODE 
  
> Les chaînes transmises sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
MSG_SERVICE_UI_READ_ONLY 
  
> L’interface utilisateur de configuration du service doit afficher la configuration actuelle, mais ne pas autoriser l’utilisateur à la modifier. 
    
SERVICE_UI_ALLOWED 
  
> Permet l’affichage d’une boîte de dialogue de configuration si nécessaire. Lorsque l SERVICE_UI_ALLOWED est définie, la boîte de dialogue ne doit s’afficher que si le tableau des valeurs de propriété  _lpProps_ est vide ou ne contient pas de configuration valide. Si SERVICE_UI_ALLOWED n’est pas définie, une boîte de dialogue peut toujours s’afficher si l’SERVICE_UI_ALWAYS est définie. 
    
UI_CURRENT_PROVIDER_FIRST 
  
> Demande que la boîte de dialogue de configuration du fournisseur actif s’affiche au-dessus des autres boîtes de dialogue. 
    
SERVICE_UI_ALWAYS 
  
> Nécessite que le service de message affiche une boîte de dialogue de configuration. Si l’indicateur SERVICE_UI_ALWAYS n’est pas définie, une boîte de dialogue de configuration peut toujours s’afficher si l’indicateur SERVICE_UI_ALLOWED est définie et que les informations de configuration valides ne sont pas disponibles dans le tableau des valeurs de propriété _lpProps._ Vous SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS être définies pour permettre l’affichage d’une interface utilisateur. 
    
 _ulContext_
  
> [in] Opération de configuration que MAPI est en train d’effectuer. Le  _paramètre ulContext_ contient l’une des valeurs suivantes : 
    
MSG_SERVICE_CONFIGURE 
  
> Les modifications apportées à la configuration du service doivent être apportées au profil. Si l’SERVICE_UI_ALWAYS est définie, le service doit afficher sa boîte de dialogue de configuration. La boîte de dialogue doit également être affichée si l’indicateur SERVICE_UI_ALLOWED est définie et que le paramètre  _lpProps_ est vide ou ne contient pas de données de configuration valides. Si  _lpProps contient_ des données valides, aucune boîte de dialogue ne doit s’afficher et le service doit utiliser ces données pour effectuer la modification de la configuration. 
    
MSG_SERVICE_CREATE 
  
> Le service est ajouté à un profil. Si l’indicateur SERVICE_UI_ALWAYS ou SERVICE_UI_ALLOWED est définie, le service doit afficher sa boîte de dialogue de configuration. Si aucun indicateur n’est définie, le service doit échouer. 
    
MSG_SERVICE_DELETE 
  
> Le service est supprimé d’un profil. Une fois cet événement reçu, le service doit S_OK.
    
MSG_SERVICE_INSTALL 
  
> Le service a été installé sur la station de travail de l’utilisateur à partir d’un réseau, d’une disquette ou d’un autre support externe. Après réception de cet événement, le service renvoie généralement S_OK. 
    
MSG_SERVICE_PROVIDER_CREATE 
  
> Demande au service de créer une instance supplémentaire d’un fournisseur. Si le service prend en charge cette opération, il doit appeler [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md). Si le service ne prend pas en charge cette opération, il peut renvoyer MAPI_E_NO_SUPPORT. 
    
MSG_SERVICE_PROVIDER_DELETE 
  
> Demande au service de supprimer une instance de fournisseur. Si le service prend en charge cette opération, il doit appeler [IProviderAdmin::D eleteProvider](iprovideradmin-deleteprovider.md). Si le service ne prend pas en charge cette opération, il peut renvoyer MAPI_E_NO_SUPPORT.
    
MSG_SERVICE_UNINSTALL 
  
> Le service est supprimé. Après avoir reçu cet événement, le service peut effectuer toutes les tâches de nettoyage qui doivent être effectuées avant la fin du service, puis retourner avec une valeur de réussite. Si l’utilisateur annule la suppression, le service doit MAPI_E_USER_CANCEL. 
    
 _cValues_
  
> [in] Nombre de valeurs de propriété dans le tableau pointés par _le paramètre lpProps._ La valeur du paramètre  _cValues_ est zéro si MAPI ne passe aucune valeur de propriété. 
    
 _lpProps_
  
> [in] Pointeur vers un tableau facultatif de structures [SPropValue](spropvalue.md) indiquant les valeurs des propriétés pris en charge par le fournisseur que la fonction utilisera lors de la configuration du service de messagerie. La fonction utilise ce paramètre uniquement si le paramètre  _ulContext_ est MSG_SERVICE_CONFIGURE. Ce paramètre est couramment utilisé pour transmettre le chemin d’accès à un fichier pour un service basé sur un fichier, tel qu’un service de carnet d’adresses personnel. Si l MSG_SERVICE_CONFIGURE n’est pas transmis dans le paramètre  _ulFlags,_ le  _paramètre lpProps_ doit être zéro. 
    
 _lpProviderAdmin_
  
> [in] Pointeur vers une interface [IProviderAdmin:IUnknown](iprovideradminiunknown.md) que la fonction peut utiliser pour localiser les sections de profil d’un fournisseur spécifique dans le service de messagerie actuel. 
    
 _lppMapiError_
  
> [out] Pointeur vers une structure [MAPIERROR.](mapierror.md) La structure est allouée avec la [fonction MAPIAllocateBuffer.](mapiallocatebuffer.md) Tous les membres sont facultatifs, bien que la plupart des structures contiennent une chaîne de message d’erreur valide dans le membre _lpszError._ Si les membres  _lpszComponent_ ou  _lpszError_ de la structure sont présents, leur mémoire doit être libérée par un seul appel à [MAPIFreeBuffer](mapifreebuffer.md) sur la structure de base. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_UNCONFIGURED 
  
> Le fournisseur de services n’a pas été configuré. 
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération, généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue. 
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur ne prend pas en charge les modifications apportées à ses objets ou ne prend pas en charge la notification des modifications. 
    
MAPI_E_BAD_CHARWIDTH 
  
> L’indicateur MAPI_UNICODE a été définie et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et l’implémentation prend uniquement en charge Unicode.
    
## <a name="remarks"></a>Remarques

Une fonction définie à l’aide du prototype de fonction **MSGSERVICEENTRY** permet aux services de message de se configurer eux-mêmes ou d’effectuer d’autres actions spécifiques au service. La fonction fournit principalement une boîte de dialogue dans laquelle l’utilisateur peut modifier les paramètres spécifiques au service de message. Il peut également prendre en charge la configuration par programme à l’aide du tableau de valeurs de propriété transmis dans le _paramètre lpProps._ La configuration par programme est facultative, sauf si le service prend en charge l’Assistant Profil, pour lequel elle est requise. 
  
MAPI appelle ce point d’entrée à partir de l’application du Panneau de configuration ou en réponse à une application cliente appelant [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) ou [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
MAPI ne place aucune restriction sur le nom de fonction qu’un service de message utilise pour le prototype **MSGSERVICEENTRY,** mais préfère le nom **ServiceEntry**. Il n’existe aucune restriction sur l’ordinal pour la fonction, et une DLL de fournisseur unique peut contenir plusieurs fonctions. Toutefois, une seule des fonctions peut être nommée **ServiceEntry**. 
  
Un service de message peut utiliser la [fonction BuildDisplayTable](builddisplaytable.md) et la méthode [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) pour simplifier l’implémentation de la boîte de dialogue de configuration. 
  
Il est possible pour un utilisateur d’annuler une MSG_SERVICE_UNINSTALL opération. Dans ce cas, la fonction **ServiceEntry** doit vérifier auprès de l’utilisateur que le service ne doit pas être supprimé et retourner MAPI_E_USER_CANCEL si le service reste installé. 
  
Une fonction basée sur le prototype **MSGSERVICEENTRY** renvoie l’une des valeurs HRESULT répertoriées. MAPI forwards this value when responding to a client’s call to [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
Les services de message qui exportent une fonction d’entrée de service doivent inclure les propriétés **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) et **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) dans la section de service de message de MAPISVC.INF. 
  

