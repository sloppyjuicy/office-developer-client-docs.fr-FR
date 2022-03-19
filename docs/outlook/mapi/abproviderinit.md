---
title: ABProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ABProviderInit
api_type:
- HeaderDef
ms.assetid: c3dcd0d4-018a-47b0-b040-227034ed59d8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b477bfb864699d305079bbe14bf7afb6db3a649c
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63629089"
---
# <a name="abproviderinit"></a>ABProviderInit

**S’applique à** : Outlook 2013 | Outlook 2016
  
Initialise un fournisseur de carnet d’adresses pour l’opération.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Implémenté par :  <br/> |Fournisseurs de carnets d’adresses  <br/> |
|Appelé par :  <br/> |MAPI  <br/> |

```cpp
HRESULT ABProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPABPROVIDER FAR * lppABProvider
);
```

## <a name="parameters"></a>Paramètres

 _hInstance_
  
> [in] Instance de la bibliothèque de liens dynamiques (DLL) du fournisseur de carnet d’adresses que MAPI a utilisée lors de sa liaison.

 _lpMalloc_
  
> [in] Pointeur vers un objet d’allocation de mémoire exposant l’interface OLE **IMalloc** . Le fournisseur de carnet d’adresses peut avoir besoin d’utiliser cette méthode d’allocation lors de l’utilisation de certaines interfaces telles que **IStream**.

 _lpAllocateBuffer_
  
> [in] Pointeur vers la [fonction MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser lorsque MAPI l’exige pour allouer de la mémoire.

 _lpAllocateMore_
  
> [in] Pointeur vers la [fonction MAPIAllocateMore](mapiallocatemore.md) , à utiliser lorsque MAPI l’exige pour allouer de la mémoire supplémentaire.

 _lpFreeBuffer_
  
> [in] Pointeur vers la [fonction MAPIFreeBuffer](mapifreebuffer.md) , à utiliser lorsque MAPI le demande pour libérer de la mémoire.

 _ulFlags_
  
> [in] Masque de bits d’indicateurs. L’indicateur suivant peut être définie :

MAPI_NT_SERVICE
  
> Le fournisseur est chargé dans le contexte d’un service Windows, un type spécial de processus sans accès à une interface utilisateur.

 _ulMAPIVer_
  
> [in] Numéro de version de l’interface de fournisseur de services (SPI) que MAPI.DLL utilise. Pour le numéro de version actuel, voir MAPISPI. Fichier d’en-tête H.

 _lpulProviderVer_
  
> [out] Pointeur vers le numéro de version du SPI utilisé par ce fournisseur de carnet d’adresses.

 _lppABProvider_
  
> [out] Pointeur vers un pointeur vers l’objet fournisseur de carnet d’adresses initialisé.

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.

MAPI_E_VERSION
  
> La version SPI utilisée par MAPI n’est pas compatible avec la spi utilisée par ce fournisseur.

## <a name="remarks"></a>Remarques

MAPI appelle la fonction de point d’entrée **ABProviderInit** pour initialiser un fournisseur de carnet d’adresses à la suite d’une inscription client.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Un fournisseur de carnet d’adresses doit **implémenter ABProviderInit en tant** que fonction de point d’entrée dans la DLL du fournisseur. L’implémentation doit être basée sur le prototype **de fonction ABPROVIDERINIT** , également spécifié dans MAPISPI.H. MAPI définit **ABPROVIDERINIT** pour utiliser le type d’appel d’initialisation MAPI standard, STDMAPIINITCALLTYPE, ce qui entraîne **ABProviderInit** à respecter la convention d’appel CDECL.
  
Un fournisseur peut être initialisé plusieurs fois, suite à l’apparition de plusieurs profils dans une utilisation simultanée ou de l’apparition de plusieurs fois dans le même profil. Étant donné que l’objet fournisseur contient du contexte, **ABProviderInit** doit retourner un autre objet fournisseur dans _lppABProvider_ pour chaque initialisation, même pour plusieurs initialisations dans le même processus.
  
Le fournisseur de carnet d’adresses doit utiliser les fonctions pointées par _lpAllocateBuffer_, _lpAllocateMore_ et _lpFreeBuffer_ pour la plupart des allocations de mémoire et de la déallocation. En particulier, le fournisseur doit utiliser ces fonctions pour allouer de la mémoire aux applications clientes lors de l’appel d’interfaces d’objets telles que [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPITable::QueryRows](imapitable-queryrows.md). Si le fournisseur s’attend également à utiliser l’allocation de mémoire OLE, il doit appeler la méthode **IUnknown::AddRef** de l’objet allocateur pointé par le paramètre _lpMalloc_ .
  
Pour plus d’informations sur l’écriture **d’ABProviderInit**, voir [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md). Pour plus d’informations sur les fonctions de point d’entrée, voir [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).
  
## <a name="see-also"></a>Consultez aussi

- [IABProvider : IUnknown](iabprovideriunknown.md)
- [MSProviderInit](msproviderinit.md)
- [XPProviderInit](xpproviderinit.md)
