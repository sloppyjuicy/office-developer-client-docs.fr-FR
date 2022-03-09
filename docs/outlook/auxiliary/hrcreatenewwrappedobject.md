---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: Crée un objet accessible par un client dans un format de caractère préféré.
ms.openlocfilehash: 4ebf64b1aa0e4ec317becb2a50a9384d3e22ee5b
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369244"
---
# <a name="hrcreatenewwrappedobject"></a>HrCreateNewWrappedObject

Crée un objet accessible par un client dans un format de caractère préféré.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exporté par :  <br/> |msmapi32.dll  <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |

```cpp
HRESULT HrCreateNewWrappedObject( 
    LPVOID        pvUnwrapped, 
    ULONG         ulUnwrappedFlags, 
    ULONG         ulWrappedFlags, 
    const IID     *pIID, 
    const ULONG   *pulReserved, 
    BOOL          fCheckWrap, 
    LPVOID       *ppvWrapped 
);

```

## <a name="parameters"></a>Paramètres

_pvUnwrapped_
  
> [in] L’objet de Outlook initialement déballé. Doit implémenter l’une des interfaces suivantes :

- [IMailUser : IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx) ou [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).

_ulUnwrappedFlags_
  
> [in] Indicateurs qui caractérisent l’objet initial non enveloppé. Doit être une ou plusieurs des valeurs suivantes :

- DDLWRAP_FLAG_ANSI — L’objet unwrapped est ANSI.

- DDLWRAP_FLAG_UNICODE— L’objet unwrapped est UNICODE.

_ulWrappedFlags_
  
> [in] Indicateurs du format de caractère préféré. Doit être une ou plusieurs des valeurs suivantes :

- DDLWRAP_FLAG_ANSI: l’objet Wrapped sera exposé en tant qu’ANSI.
- DDLWRAP_FLAG_UNICODE: l’objet Wrapped sera exposé en tant qu’UNICODE.

_pIID_
  
> [in] Identificateur de l’interface pris en charge par l’objet déballé ; définissez-la sur NULL si ce n’est pas le cas.

_agiReserved_
  
> [in] Ce paramètre n’est pas utilisé. Elle doit être NULL.

_fCheckWrap_
  
> [in] Définissez ce paramètre sur **true si** _pvUnwrapped_ doit être vérifié pour son format avant l’habillage ; si **l’objet** doit être wrapped sans vérification.

_ppvWrapped_
  
> [out] Pointeur vers l’objet demandé, wrapped dans le format de caractère demandé.

## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Remarques

La transmission d’un objet wrapped avec _fCheckWrap_ définie sur **true** entraîne un objet non enveloppé. Que l’objet renvoyé soit wrapped ou non, le client est responsable de la libération de la référence sur l’objet renvoyé.
  
Lorsque vous **utilisez GetProcAddress** pour rechercher l’adresse de cette fonction dans msmapi32.dll, spécifiez **HrCreateNewWrappedObject@28** comme nom de procédure.
  
## <a name="see-also"></a>Voir aussi

- [À propos de la couche de dégradation de données API](about-the-data-degradation-layer-api.md)
- [Constantes (API de couche de dégradation des données)](constants-data-degradation-layer-api.md)
