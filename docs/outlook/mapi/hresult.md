---
title: HRESULT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: b248ed11-3d8a-4d4c-9b84-fa5bee7979c7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ee2ef6d3f8b61c5cf140f29fb97342033b4777a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571933"
---
# <a name="hresult"></a>HRESULT

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valeur 32 bits utilisée pour décrire une erreur ou un avertissement.
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a>Remarques

Le type de données **HRESULT** est identique au type de données [SCODE.](scode.md) 
  
Une **valeur HRESULT** se compose des champs suivants : 
  
- Code 1 bit indiquant la gravité, où zéro représente la réussite et 1 représente l’échec.
    
- Valeur réservée 4 bits.
    
- Code 11 bits indiquant la responsabilité de l’erreur ou de l’avertissement, également appelé code d’installation.
    
- Code 16 bits décrivant l’erreur ou l’avertissement.
    
La plupart des méthodes et fonctions d’interface MAPI retournent des **valeurs HRESULT** pour fournir une formation de cause détaillée. **Les valeurs HRESULT** sont également largement utilisées dans les méthodes d’interface OLE. OLE fournit plusieurs macros pour la conversion entre les valeurs **HRESULT** et les valeurs **SCODE,** un autre type de données courant pour la gestion des erreurs. 
  
> [!NOTE]
> Dans MAPI 64 bits, **HRESULT** est toujours une valeur 32 bits. 
  
Pour plus d’informations sur l’utilisation OLE des valeurs **HRESULT,** voir la *référence du programmeur OLE.* Pour plus d’informations sur l’utilisation de ces valeurs dans MAPI, voir [Gestion](error-handling-in-mapi.md) des erreurs et l’une des méthodes d’interface suivantes : 
  
[IABLogon::GetLastError](iablogon-getlasterror.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[IMAPIControl::GetLastError](imapicontrol-getlasterror.md)
  
[IMAPITable::GetLastError](imapitable-getlasterror.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIViewAdviseSink::OnPrint](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a>Voir aussi



[SCODE](scode.md)


[Types de données MAPI](mapi-data-types.md)

