---
title: MAPIERROR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIERROR
api_type:
- COM
ms.assetid: e04c2228-aa0a-4958-b5b2-6467e93ab613
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: bbf8e2eb2961a3d149010b876d2b4cb3d0c8abc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592527"
---
# <a name="mapierror"></a>MAPIERROR

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Fournit des informations détaillées sur une erreur, généralement générée par le système d’exploitation, MAPI ou un fournisseur de services. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _MAPIERROR
{
  ULONG ulVersion;
  LPSTR lpszError;
  LPSTR lpszComponent;
  ULONG ulLowLevelError;
  ULONG ulContext;
} MAPIERROR, FAR * LPMAPIERROR;

```

## <a name="members"></a>Members

 **ulVersion**
  
> Numéro de version de la structure. Le membre **ulVersion** est utilisé pour l’extension future et doit être défini avec MAPI_ERROR_VERSION, qui est actuellement défini comme zéro. 
    
 **lpszError**
  
> Pointeur vers une chaîne qui décrit l’erreur. Si le paramètre _ulFlags_ à la méthode dans laquelle cette structure est utilisée est défini sur MAPI_UNICODE, cette chaîne sera au format Unicode. 
    
 **lpszComponent**
  
> Pointeur vers une chaîne qui décrit le composant qui a généré l’erreur. Si le paramètre _ulFlags_ à la méthode dans laquelle cette structure est utilisée est défini sur MAPI_UNICODE, cette chaîne sera au format Unicode. 
    
 **ulLowLevelError**
  
> Valeur d’erreur de bas niveau est utilisé uniquement lorsque l’erreur à renvoyer est bas niveau.
    
 **ulContext**
  
> Valeur qui représente l’emplacement dans le composant indiqué par le membre **lpszComponent** qui identifie où l’erreur s’est produite. 
    
## <a name="remarks"></a>Remarques

La structure **MAPIERROR** est utilisée pour décrire les informations d’erreur. Clients et fournisseurs de services de passer un pointeur vers une structure **MAPIERROR** dans le paramètre _lppMAPIError_ de la méthode [IMAPIProp::GetLastError](imapiprop-getlasterror.md) . **GetLastError** retourne des informations sur l’erreur précédente s’est produite à un objet. Les appelants de **GetLastError** libérer de la mémoire pour la structure **MAPIERROR** en appelant [MAPIFreeBuffer](mapifreebuffer.md).
  
Le membre de **lpszComponent** peut être utilisé pour mapper le fichier d’aide du composant, si elle existe. Fournisseurs de service doivent limiter la taille de la chaîne de composant à 30 caractères afin qu’elle peut être facilement affichée dans une boîte de dialogue. Le membre **ulContext** peut également servir pour faire référence à une rubrique d’aide en ligne pour les erreurs courantes. 
  
Étant donné que les fournisseurs de services ne sont pas requis pour fournir des informations d’erreur détaillé, clients attendez pas un des membres de la structure **MAPIERROR** qui sont renvoyées pour contenir des données valides. Toutefois, à une minimum MAPI recommande que fournisseurs de spécifier des informations dans les membres **lpszComponent** et **ulContext** . 
  
Pour plus d’informations sur la gestion des erreurs dans MAPI, consultez [Gestion des erreurs](error-handling-in-mapi.md).
  
## <a name="see-also"></a>Voir aussi



[IABLogon::GetLastError](iablogon-getlasterror.md)
  
[IABProvider::Logon](iabprovider-logon.md)
  
[IMAPIControl::GetLastError](imapicontrol-getlasterror.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPISession::GetLastError](imapisession-getlasterror.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md)
  
[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)
  
[IMAPITable::GetLastError](imapitable-getlasterror.md)
  
[IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md)
  
[IMSLogon::GetLastError](imslogon-getlasterror.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[IProfAdmin::GetLastError](iprofadmin-getlasterror.md)
  
[IProviderAdmin::GetLastError](iprovideradmin-getlasterror.md)


[Structures MAPI](mapi-structures.md)

