---
title: HrGetAutoDiscoverXML
description: Cet article décrit la fonction HrGetAutoDiscoverXML et fournit la syntaxe, les paramètres et la valeur de retour.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- HrGetAutoDiscoverXML
api_type:
- COM
ms.assetid: 03691187-7c65-620b-576f-6ebe62a80830
ms.openlocfilehash: 9cce4c89f08e98bd35237543839fe51f86e0d6fc
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817899"
---
# <a name="hrgetautodiscoverxml"></a>HrGetAutoDiscoverXML

**S’applique à** : Outlook 2013 | Outlook 2016

Retourne un flux XML (Extensible Markup Language) qui représente les informations récupérées à partir du service de découverte automatique d’un serveur Microsoft Exchange 2007.

## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Exporté par :  <br/> |olmapi32.dll  <br/> |
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

> [in] Adresse de messagerie SMTP (Simple Mail Transfer Protocol) terminée par une valeur Null du compte pour lequel vous souhaitez récupérer les informations de découverte automatique.

 _pwzPassword_

> [in] Mot de passe facultatif pour le compte spécifié par _pwzAddress_. Notez que le passage d’un mot de passe n’a aucun effet si le compte spécifié par  _pwzAddress_ ne nécessite pas de mot de passe.

 _hCancelEvent_

> [in] Handle d’événement Win32 non défini qui est facultatif et peut être utilisé pour annuler l’opération. Pour annuler l’opération, définissez l’événement et transmettez le handle d’événement en tant que _hCancelEvent_ ; passe la **valeur null** si vous ne souhaitez pas annuler l’opération. Notez que le passage d’une valeur qui ne représente pas un handle d’événement n’a aucun effet et est ignoré par la fonction.

 _ulFlags_

> [in] Ce paramètre n’est pas utilisé. Il doit être 0.

 _ppXmlStream_

> [out] Pointeur vers un objet [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) qui contient le code XML de découverte automatique. Retourne **null** si l’opération de découverte automatique échoue. Vous devez libérer l’objet [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) une fois que vous en avez terminé avec celui-ci.

## <a name="return-values"></a>Valeurs de retour

S_OK

- L’appel de fonction réussit.

E_INVALIDARG

- _pwzAddress_ est **null** ou n’est pas une adresse SMTP valide, ou _ppXmlStream_ est un pointeur **null** vers un objet [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) .

MAPI_E_NOT_FOUND

- L’ordinateur client n’est pas connecté au réseau, l’ordinateur client n’est pas connecté à un serveur Microsoft Exchange 2007, _pwzAddress_ n’est pas un compte sur un serveur Exchange 2007 ou _pwzAddress_ est un compte qui ne prend pas en charge Exchange service de découverte automatique.

MAPI_E_USER_CANCEL

- Un handle d’événement a été passé à _hCancelEvent_ pour annuler l’opération.

STRSAFE_E_INSUFFICIENT_BUFFER

- La valeur passée à _pwzAddress_ ou _pwzPassword_ est trop longue, de sorte qu’elle dépasse la mémoire tampon interne de taille 256 octets.
