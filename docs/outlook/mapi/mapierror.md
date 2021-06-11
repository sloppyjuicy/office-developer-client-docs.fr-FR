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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 682e75c4e0a2f60dbd46a13b0b737ca4a8e18f3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409145"
---
# <a name="mapierror"></a>MAPIERROR

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
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
  
> Numéro de version de la structure. Le **membre ulVersion** est utilisé pour l’expansion future et doit être défini sur MAPI_ERROR_VERSION, qui est actuellement défini sur zéro. 
    
 **lpszError**
  
> Pointeur vers une chaîne qui décrit l’erreur. Cette chaîne sera au format Unicode si le paramètre  _ulFlags_ de la méthode dans laquelle cette structure est utilisée est MAPI_UNICODE. 
    
 **lpszComponent**
  
> Pointeur vers une chaîne qui décrit le composant qui a généré l’erreur. Cette chaîne sera au format Unicode si le paramètre  _ulFlags_ de la méthode dans laquelle cette structure est utilisée est MAPI_UNICODE. 
    
 **ulLowLevelError**
  
> Valeur d’erreur de bas niveau utilisée uniquement lorsque l’erreur à retourner est de bas niveau.
    
 **ulContext**
  
> Valeur qui représente l’emplacement dans le composant pointé par le membre **lpszComponent** qui identifie l’endroit où l’erreur s’est produite. 
    
## <a name="remarks"></a>Remarques

La structure **MAPIERROR** est utilisée pour décrire les informations d’erreur. Les clients et les fournisseurs de services passent un pointeur vers une structure **MAPIERROR** dans le paramètre _lppMAPIError_ de la méthode [IMAPIProp::GetLastError.](imapiprop-getlasterror.md) **GetLastError renvoie des** informations sur l’erreur précédente qui s’est produite sur un objet. Les appelants **de GetLastError** libèrent la mémoire de la structure **MAPIERROR** en appelant [MAPIFreeBuffer](mapifreebuffer.md).
  
Le **membre lpszComponent** peut être utilisé pour macalculer le fichier d’aide du composant, s’il en existe un. Les fournisseurs de services doivent limiter la taille de la chaîne de composant à 30 caractères afin qu’elle puisse s’afficher facilement dans une boîte de dialogue. Le **membre ulContext** peut également être utilisé pour faire référence à une rubrique d’aide en ligne pour les erreurs courantes. 
  
Étant donné que les fournisseurs de services ne sont pas tenus de fournir des informations détaillées sur les erreurs, les clients ne doivent pas s’attendre à ce que les membres de la structure **MAPIERROR** retournés contiennent des données valides. Toutefois, MAPI recommande vivement aux fournisseurs de spécifier des informations dans les membres **lpszComponent** et **ulContext.** 
  
Pour plus d’informations sur la gestion des erreurs dans MAPI, voir [Gestion des erreurs.](error-handling-in-mapi.md)
  
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

