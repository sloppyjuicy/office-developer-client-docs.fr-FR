---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: Crée un objet qui peut accéder à un client dans un format de caractère par défaut.
ms.openlocfilehash: 187bcbce8fd1170e05f57c5c9147a8962669fea4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782565"
---
# <a name="hrcreatenewwrappedobject"></a>HrCreateNewWrappedObject

Crée un objet qui peut accéder à un client dans un format de caractère par défaut.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exportés par :  <br/> |Msmapi32.dll  <br/> |
|Appelée par :  <br/> |Client  <br/> |
|Implémentée par :  <br/> |Outlook  <br/> |
   
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
  
> [in] L’objet Outlook non initiale. Doit implémenter une des interfaces suivantes :
    
   - [IMailUser : IMAPIProp](http://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](http://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](http://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](http://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](http://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), ou [IOSTX](http://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).
    
_ulUnwrappedFlags_
  
> [in] Indicateurs qui caractérisent l’objet initial non. Doit être une ou plusieurs des valeurs suivantes :
    
   - DDLWRAP_FLAG_ANSI : objet Unwrapped est au format ANSI.
    
   - DDLWRAP_FLAG_UNICODE : objet Unwrapped est au format UNICODE.
    
_ulWrappedFlags_
  
>  [in] Indicateurs pour le format de caractères par défaut. Doit être une ou plusieurs des valeurs suivantes : 
    
   - DDLWRAP_FLAG_ANSI : objet Wrapped est exposé en tant que ANSI.
    
   - DDLWRAP_FLAG_UNICODE : objet Wrapped est exposé au format UNICODE.
    
_pIID_
  
>  [in] L’identificateur de l’interface pris en charge par l’objet non ; valeur NULL s’il s’agit inconnu. 
    
_pulReserved_
  
>  [in] Ce paramètre n’est pas utilisé. Il doit être NULL. 
    
_fCheckWrap_
  
>  [in] Définissez ce paramètre sur **true** si _pvUnwrapped_ doit être vérifiée pour son format avant le retour à la ligne ; valeur **false** si l’objet doit être entourée sans vérification. 
    
_ppvWrapped_
  
>  [out] Pointeur vers l’objet demandé, incluse dans le format de caractères demandé. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Note

Passage d’un objet encapsulé avec _fCheckWrap_ défini sur **true** entraînera un objet non. Quel que soit ou non l’objet retourné est encapsulé, le client est chargé de libérer la référence de l’objet renvoyé. 
  
Lorsque vous utilisez **GetProcAddress** pour rechercher l’adresse de cette fonction dans msmapi32.dll, spécifiez **HrCreateNewWrappedObject@28** comme nom de la procédure. 
  
## <a name="see-also"></a>Voir aussi

- [À propos de la couche de dégradation de données API](about-the-data-degradation-layer-api.md)
- [Constantes (couche de dégradation de données API)](constants-data-degradation-layer-api.md)

