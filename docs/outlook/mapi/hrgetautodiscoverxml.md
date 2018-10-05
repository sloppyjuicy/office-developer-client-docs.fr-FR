---
title: HrGetAutoDiscoverXML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetAutoDiscoverXML
api_type:
- COM
ms.assetid: 03691187-7c65-620b-576f-6ebe62a80830
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 77f28654ffe0f6f459fde229bb7428f2c39e96c0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400718"
---
# <a name="hrgetautodiscoverxml"></a>HrGetAutoDiscoverXML

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie un flux Extensible Markup Language (XML) qui représente les informations récupérées à partir du service de découverte automatique d’un serveur Microsoft Exchange 2007.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exportés par :  <br/> |olmapi32.dll  <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
   
```cpp
HRESULT HrGetAutoDiscoverXML( 
    __in_z const WCHAR *pwzAddress, 
    __in_opt_z const WCHAR *pwzPassword, 
    __in_opt HANDLE hCancelEvent, 
    __in_opt ULONG ulFlags, 
    __out IStream** ppXmlStream); 

```

## <a name="parameters"></a>Paramètres

 _pwzAddress_
  
> [in] Une caractère nul SMTP Simple Mail Transfer Protocol () adresse de messagerie du compte pour lequel vous souhaitez récupérer les informations de découverte automatique.
    
 _pwzPassword_
  
> [in] Un mot de passe facultatif pour le compte spécifié par _pwzAddress_. Notez que n’importe quel mot de passe est sans effet si le compte spécifié par _pwzAddress_ ne requiert pas un mot de passe. 
    
 _hCancelEvent_
  
> [in] Un cadre Win32 handle d’événement qui est facultatif et peut être utilisé pour annuler l’opération. Pour annuler l’opération, définissez l’événement et passer le descripteur d’événement comme _hCancelEvent_; Passez la **valeur null** si vous ne souhaitez pas annuler l’opération. Notez que le passage d’une valeur qui ne représente pas un handle d’événement n’a aucun effet et est ignorée par la fonction. 
    
 _ulFlags_
  
> [in] Ce paramètre n’est pas utilisé. Il doit être 0.
    
 _ppXmlStream_
  
> [out] Pointeur vers un objet [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) qui contient la XML de découverte automatique. Renvoie la **valeur null** en cas d’échec de l’opération de découverte automatique. Vous devez libérer l’objet [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) lorsque vous avez terminé avec lui. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK 
  
- L’appel de fonction a réussi.
    
E_INVALIDARG 
  
-  _pwzAddress_ est **null** ou n’est pas une adresse SMTP valide ou _ppXmlStream_ est un pointeur vers un objet [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) **null** . 
    
MAPI_E_NOT_FOUND 
  
- Ordinateur client n’est pas connecté au réseau, ordinateur client n’est pas connecté à un serveur Microsoft Exchange 2007, _pwzAddress_ n’est pas un compte sur un serveur Exchange 2007 ou _pwzAddress_ est un compte qui ne prend pas en charge Exchange service de découverte automatique. 
    
MAPI_E_USER_CANCEL 
  
- Un handle d’événement a été passé à _hCancelEvent_ pour annuler l’opération. 
    
STRSAFE_E_INSUFFICIENT_BUFFER
  
- La valeur transmise à _pwzAddress_ ou _pwzPassword_ est trop longue, tels que les cas de dépassement de la mémoire tampon interne de 256 octets. 
    

