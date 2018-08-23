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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 954609cbc62039c0d60874bde83fde50d1d11c30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591666"
---
# <a name="msgserviceentry"></a>MSGSERVICEENTRY

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Définit un prototype pour une fonction point d’entrée message service prendre en charge la configuration du service de message. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Fonction implémentée par :  <br/> |Services de messagerie  <br/> |
|Fonction appelée par :  <br/> |MAPI  <br/> |
   
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
  
> [in] Handle de l’instance de le providerDLL service. La poignée est généralement utilisée pour récupérer des ressources. 
    
 _lpMalloc_
  
> [in] Pointeur vers un objet d’allocation mémoire exposant l’interface OLE **IMalloc** . Le service de message devrez peut-être utiliser cette méthode de répartition lorsque vous travaillez avec certaines interfaces comme **IStream**. 
    
 _lpMAPISup_
  
> [in] Pointeur vers une [IMAPISupport : IUnknown](imapisupportiunknown.md) implémentation de l’interface. 
    
 _ulUIParam_
  
> [in] Une valeur spécifique à l’implémentation utilisée pour transmettre des informations d’interface utilisateur à une fonction ou à zéro. Le paramètre _ulUIParam_ est le handle de fenêtre parent pour la boîte de dialogue de configuration et de type HWND (cast à un ULONG_PTR entière). La valeur zéro indique qu’il n’existe aucune fenêtre parent. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs indiquant les options pour la fonction de l’entrée de service. Les indicateurs suivants peuvent être définis :
    
MAPI_UNICODE 
  
> Les chaînes passée sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
MSG_SERVICE_UI_READ_ONLY 
  
> Interface utilisateur de configuration du service doit afficher la configuration actuelle, mais pas autoriser l’utilisateur à modifier. 
    
SERVICE_UI_ALLOWED 
  
> Permet à une boîte de dialogue de configuration à afficher si nécessaire. Lors de l’indicateur SERVICE_UI_ALLOWED est défini, la boîte de dialogue doit être affichée uniquement si le tableau de valeurs de propriété _lpProps_ est vide ou ne contient-elle pas une configuration valide. Si SERVICE_UI_ALLOWED n’est pas défini, une boîte de dialogue peut toujours être affichée si l’indicateur SERVICE_UI_ALWAYS est défini. 
    
UI_CURRENT_PROVIDER_FIRST 
  
> Demande que la boîte de dialogue configuration pour le fournisseur active affiche par-dessus les autres boîtes de dialogue. 
    
SERVICE_UI_ALWAYS 
  
> Requiert le service de message pour afficher une boîte de dialogue de configuration. Si l’indicateur SERVICE_UI_ALWAYS n’est pas définie, une boîte de dialogue configuration peut toujours être affichée si l’indicateur SERVICE_UI_ALLOWED est défini et que les informations de configuration valides ne sont pas disponibles dans le tableau de valeurs de propriété _lpProps_ . SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS doit être définie pour autoriser une interface utilisateur à afficher. 
    
 _ulContext_
  
> [in] L’opération de configuration MAPI exécute actuellement. Le paramètre _ulContext_ contient une des valeurs suivantes : 
    
MSG_SERVICE_CONFIGURE 
  
> Modifications apportées à la configuration du service doivent être effectuées dans le profil. Si l’indicateur SERVICE_UI_ALWAYS est défini, le service doit afficher la boîte de dialogue de configuration. La boîte de dialogue doit également être affichée si l’indicateur SERVICE_UI_ALLOWED est défini et que le paramètre _lpProps_ est vide ou ne contient-elle pas de données de configuration valides. Si _lpProps_ contient des données valides, aucune boîte de dialogue ne doit s’afficher et le service doit utiliser ces données pour effectuer la modification de configuration. 
    
MSG_SERVICE_CREATE 
  
> Le service est ajouté à un profil. Si l’indicateur SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS est défini, le service doit afficher la boîte de dialogue de configuration. Si aucun indicateur n’est défini, le service doit échouer. 
    
MSG_SERVICE_DELETE 
  
> Le service est en cours de suppression d’un profil. Après avoir reçu cet événement, le service doit renvoyer S_OK.
    
MSG_SERVICE_INSTALL 
  
> Le service a été installé sur le poste de travail à partir d’un réseau, disquette ou autre support externe. Après avoir reçu cet événement, le service renvoie généralement S_OK. 
    
MSG_SERVICE_PROVIDER_CREATE 
  
> Demande que le service crée une instance supplémentaire d’un fournisseur. Si le service prend en charge cette opération, il doit appeler [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md). Si le service ne prend pas en charge cette opération, il peut retourner MAPI_E_NO_SUPPORT. 
    
MSG_SERVICE_PROVIDER_DELETE 
  
> Demande que le service de supprime une instance de fournisseur. Si le service prend en charge cette opération, il doit appeler [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md). Si le service ne prend pas en charge cette opération, il peut retourner MAPI_E_NO_SUPPORT.
    
MSG_SERVICE_UNINSTALL 
  
> Le service est en cours de suppression. Après avoir reçu cet événement, le service peut effectuer des tâches de nettoyage qui doivent être effectuées avant le service se termine et puis renvoie une valeur de réussite. Si l’utilisateur annule la suppression, le service doit retourner MAPI_E_USER_CANCEL. 
    
 _cValues_
  
> [in] Nombre de valeurs de propriété dans le tableau indiqué par le paramètre _lpProps_ . La valeur du paramètre _cValues_ est égale à zéro si MAPI ne transmet aucune valeur de propriété. 
    
 _lpProps_
  
> [in] Pointeur vers un tableau facultatif de [SPropValue](spropvalue.md) structures indiquant les valeurs des propriétés de fournisseur pris en charge qui utilise la fonction de la configuration du service de message. La fonction utilise uniquement ce paramètre si le paramètre _ulContext_ est défini sur MSG_SERVICE_CONFIGURE. Ce paramètre est généralement utilisé pour transmettre le chemin d’accès à un fichier pour un service basé sur le fichier, comme un service de carnet d’adresses personnel. Si l’indicateur MSG_SERVICE_CONFIGURE n’est pas transmis dans le paramètre _ulFlags_ , le paramètre _lpProps_ doit être égal à zéro. 
    
 _lpProviderAdmin_
  
> [in] Pointeur vers une interface [IProviderAdmin:IUnknown](iprovideradminiunknown.md) que la fonction peut utiliser pour rechercher les sections de profil pour un fournisseur spécifique dans le service de message en cours. 
    
 _lppMapiError_
  
> [out] Pointeur vers une structure [MAPIERROR](mapierror.md) . La structure est allouée avec la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) . Tous les membres sont facultatifs, bien que la plupart des structures contient une chaîne de message d’erreur valide dans le membre _lpszError_ . Si les membres _lpszComponent_ ou _lpszError_ de la structure sont présentes, leur mémoire doit finalement libérée par un simple appel à [MAPIFreeBuffer](mapifreebuffer.md) sur la structure de base. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_UNCONFIGURED 
  
> Le fournisseur de services n’a pas été configuré. 
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue. 
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur ne prend pas en charge les modifications apportées à ses objets ou ne prend pas en charge la notification des modifications. 
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend uniquement en charge Unicode.
    
## <a name="remarks"></a>Remarques

Une fonction définie à l’aide du prototype de la fonction **MSGSERVICEENTRY** permet de services de messagerie pour configurer eux-mêmes ou pour effectuer d’autres actions spécifiques au service. La fonction fournit principalement une boîte de dialogue dans laquelle l’utilisateur peut modifier les paramètres spécifiques au service de message. Il peut également prendre en charge de configuration par programme en utilisant le tableau de valeurs de propriété passé dans le paramètre _lpProps_ . Configuration par programme est facultative, sauf si le service prend en charge l’Assistant profil, pour laquelle il est nécessaire. 
  
Les appels MAPI ce point d’entrée de l’application du Panneau de configuration ou en réponse à une application cliente appelant [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) ou [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
MAPI ne place aucune restriction sur le nom de la fonction qu’un service de message utilise pour le prototype **MSGSERVICEENTRY** mais préfère le nom **ServiceEntry**. Il n’existe aucune restriction sur le nombre ordinal de la fonction et un fournisseur unique DLL peut contenir plusieurs fonctions. Toutefois, une seule des fonctions peut être nommée **ServiceEntry**. 
  
Un service de message peut utiliser la fonction [BuildDisplayTable](builddisplaytable.md) et la méthode [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) pour simplifier l’implémentation de boîte de dialogue de configuration. 
  
Il est possible pour un utilisateur d’annuler une opération MSG_SERVICE_UNINSTALL. Dans ce cas, la fonction **ServiceEntry** doit vérifier avec l’utilisateur pour vérifier que le service ne doivent pas être supprimés et renvoyer MAPI_E_USER_CANCEL si le service est toujours installé. 
  
Une fonction basée sur le prototype **MSGSERVICEENTRY** renvoie une des valeurs HRESULT répertoriées. MAPI transfère cette valeur lors de la réponse à l’appel d’un client à [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
Services de messagerie à exporter une fonction d’entrée de service doivent inclure le **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) et les propriétés de **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) dans la section service de message de MAPISVC.INF. 
  

