---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: Crée un objet auquel un client peut accéder dans un format de caractères préféré.
ms.openlocfilehash: 3f68e0f275bcc5df065b3113d3322d6957f76df0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317604"
---
# <a name="hrcreatenewwrappedobject"></a>HrCreateNewWrappedObject

Crée un objet auquel un client peut accéder dans un format de caractères préféré.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exporté par:  <br/> |msmapi32. dll  <br/> |
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
  
> dans Objet Outlook initial non encapsulé. Doit implémenter l'une des interfaces suivantes:
    
   - [IMailUser: IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder: IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage: IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore: IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), IMSLogon [: IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx)ou [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).
    
_ulUnwrappedFlags_
  
> dans Indicateurs qui caractérisent l'objet initial non encapsulé. Doit être une ou plusieurs des valeurs suivantes:
    
   - DDLWRAP_FLAG_ANSI: l'objet non encapsulé est au format ANSI.
    
   - DDLWRAP_FLAG_UNICODE: l'objet non encapsulé est UNICODE.
    
_ulWrappedFlags_
  
>  dans Indicateurs pour le format de caractères par défaut. Doit être une ou plusieurs des valeurs suivantes: 
    
   - DDLWRAP_FLAG_ANSI: l'objet encapsulé sera exposé en tant que ANSI.
    
   - DDLWRAP_FLAG_UNICODE: l'objet encapsulé sera exposé en tant que UNICODE.
    
_pIID_
  
>  dans Identificateur de l'interface pris en charge par l'objet déencapsulé; Définissez-la sur NULL si cette valeur est inconnue. 
    
_pulReserved_
  
>  dans Ce paramètre n'est pas utilisé. Elle doit être NULL. 
    
_fCheckWrap_
  
>  dans Définissez ce paramètre sur **true** si la mise en forme de _pvUnwrapped_ doit être vérifiée avant l'encapsulation; Affectez- **** lui la valeur false si l'objet doit être encapsulé sans vérification. 
    
_ppvWrapped_
  
>  remarquer Pointeur vers l'objet demandé, encapsulé dans le format de caractère demandé. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Remarques

Le passage d'un objet encapsulé avec _fCheckWrap_ défini sur **true** génère un objet non encapsulé. Que l'objet renvoyé soit ou non encapsulé, le client est responsable de la publication de la référence sur l'objet renvoyé. 
  
Lors de l'utilisation de **GetProcAddress** pour Rechercher l'adresse de cette fonction dans msmapi32. dll, spécifiez **HrCreateNewWrappedObject @ 28** comme nom de procédure. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de la couche de dégradation de données API](about-the-data-degradation-layer-api.md)
- [Constantes (API de la couche de dégradation des données)](constants-data-degradation-layer-api.md)

