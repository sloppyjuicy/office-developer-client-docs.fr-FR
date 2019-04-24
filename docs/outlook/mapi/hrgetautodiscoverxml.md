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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 77f28654ffe0f6f459fde229bb7428f2c39e96c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347802"
---
# <a name="hrgetautodiscoverxml"></a>HrGetAutoDiscoverXML

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie un flux XML (Extensible Markup Language) qui représente des informations extraites du service de découverte automatique d'un serveur Microsoft Exchange 2007.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exporté par:  <br/> |olmapi32. dll  <br/> |
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
  
> dans Adresse de messagerie SMTP (Simple Mail Transfer Protocol) du compte pour lequel vous souhaitez récupérer les informations de découverte automatique.
    
 _pwzPassword_
  
> dans Mot de passe facultatif pour le compte spécifié par _pwzAddress_. Notez que le passage de n'importe quel mot de passe n'a aucun effet si le compte spécifié par _pwzAddress_ ne requiert pas de mot de passe. 
    
 _hCancelEvent_
  
> dans Un descripteur d'événement Win32 non défini qui est facultatif et qui peut être utilisé pour annuler l'opération. Pour annuler l'opération, définissez l'événement et transmettez le descripteur d'événement en tant que _hCancelEvent_; transmettez la **valeur null** si vous ne souhaitez pas annuler l'opération. Notez que le passage d'une valeur qui ne représente pas un descripteur d'événement n'a aucun effet et est ignoré par la fonction. 
    
 _ulFlags_
  
> dans Ce paramètre n'est pas utilisé. Il doit être égal à 0.
    
 _ppXmlStream_
  
> remarquer Pointeur vers un objet [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) qui contient le code XML de découverte automatique. Renvoie la **valeur null** si l'opération de découverte automatique échoue. Vous devez libérer l'objet [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) une fois que vous avez terminé. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK 
  
- L'appel de fonction est réussi.
    
E_INVALIDARG 
  
-  _pwzAddress_ est **null** ou n'est pas une adresse SMTP valide, ou _ppXmlStream_ est un pointeur **null** vers un objet [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) . 
    
MAPI_E_NOT_FOUND 
  
- L'ordinateur client n'est pas connecté au réseau, l'ordinateur client n'est pas connecté à un serveur Microsoft Exchange 2007, _pwzAddress_ n'est pas un compte sur un serveur Exchange 2007 ou _pwzAddress_ est un compte qui ne prend pas en charge Exchange service de découverte automatique. 
    
MAPI_E_USER_CANCEL 
  
- Un descripteur d'événement a été transmis à _hCancelEvent_ pour annuler l'opération. 
    
STRSAFE_E_INSUFFICIENT_BUFFER
  
- La valeur transmise à _pwzAddress_ ou _pwzPassword_ est trop longue, de sorte qu'elle déborde de la mémoire tampon interne de taille 256 octets. 
    

