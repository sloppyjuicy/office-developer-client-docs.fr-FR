---
title: HRESULT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: b248ed11-3d8a-4d4c-9b84-fa5bee7979c7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a3e46732f9b74b9cdf2dc4c961e7b6b66e3d91d4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565227"
---
# <a name="hresult"></a>HRESULT

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Une valeur de 32 bits qui est utilisée pour décrire une erreur ou un avertissement.
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a>Remarques

Le type de données **HRESULT** est la même que le type de données [SCODE](scode.md) . 
  
Une valeur **HRESULT** comprend les champs suivants : 
  
- Un code de 1 bit qui indique le niveau de gravité, où zéro réussite 1 représente et échec.
    
- Une valeur réservée 4 bits.
    
- Un code 11 bits indiquant la responsabilité de l’erreur ou avertissement, également connu sous le nom d’un code de fonction.
    
- Un code décrivant l’erreur ou avertissement de 16 bits.
    
La plupart des fonctions et les méthodes d’interface MAPI retournent les valeurs **HRESULT** pour fournir la formation cause détaillée. Les valeurs **HRESULT** sont également utilisés largement dans les méthodes d’interface OLE. OLE fournit plusieurs macros pour la conversion entre les valeurs **HRESULT** et **SCODE** , des types de données communes une autre pour la gestion des erreurs. 
  
> [!NOTE]
> 64 bits, MAPI, **HRESULT** est toujours une valeur 32 bits. 
  
Pour plus d’informations sur l’utilisation OLE de valeurs **HRESULT** , voir la *référence du programmeur OLE* . Pour plus d’informations sur l’utilisation de ces valeurs dans MAPI, voir [Gestion des erreurs](error-handling-in-mapi.md) et une des méthodes d’interface suivantes : 
  
[IABLogon::GetLastError](iablogon-getlasterror.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[IMAPIControl::GetLastError](imapicontrol-getlasterror.md)
  
[IMAPITable::GetLastError](imapitable-getlasterror.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIViewAdviseSink::OnPrint](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a>Voir aussi



[SCODE](scode.md)


[Types de données MAPI](mapi-data-types.md)

