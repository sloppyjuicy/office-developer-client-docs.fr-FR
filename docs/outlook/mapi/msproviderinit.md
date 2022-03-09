---
title: MSProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MSProviderInit
api_type:
- HeaderDef
ms.assetid: 230c66c4-ab04-4fa6-946f-9f4b704f2842
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e37a4006b800bc0a43e1f417fdd89ca22b356f8b
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376174"
---
# <a name="msproviderinit"></a>MSProviderInit

**S’applique à** : Outlook 2013 | Outlook 2016
  
Initialise un fournisseur de magasins de messages pour l’opération.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Implémenté par :  <br/> |Fournisseurs de magasins de messages  <br/> |
|Appelé par :  <br/> |MAPI  <br/> |

```cpp
HRESULT MSProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPMSPROVIDER FAR * lppMSProvider
);
```

## <a name="parameters"></a>Paramètres

 _hInstance_
  
> [in] Instance de la bibliothèque de liens dynamiques (DLL) du fournisseur de magasins de messages que MAPI a utilisée lors de sa liaison.

 _lpMalloc_
  
> [in] Pointeur vers un objet d’allocation de mémoire exposant l’interface OLE **IMalloc** . Le fournisseur de magasin de messages peut avoir besoin d’utiliser cette méthode d’allocation lors de l’utilisation de certaines interfaces telles que **IStream**.

 _lpAllocateBuffer_
  
> [in] Pointeur vers la [fonction MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser pour allouer de la mémoire.

 _lpAllocateMore_
  
> [in] Pointeur vers la [fonction MAPIAllocateMore](mapiallocatemore.md) , à utiliser pour allouer de la mémoire supplémentaire.

 _lpFreeBuffer_
  
> [in] Pointeur vers la [fonction MAPIFreeBuffer](mapifreebuffer.md) , à utiliser pour libérer de la mémoire.

 _ulFlags_
  
> [in] Masque de bits d’indicateurs. L’indicateur suivant peut être définie :

MAPI_NT_SERVICE
  
> Le fournisseur est chargé dans le contexte d’un service Windows, un type spécial de processus sans accès à une interface utilisateur.

 _ulMAPIVer_
  
> [in] Numéro de version de l’interface de fournisseur de services (SPI) que MAPI utilise. Pour le numéro de version actuel, voir le fichier d’en-tête Mapispi.h.

 _lpulProviderVer_
  
> [out] Pointeur vers le numéro de version du spi utilisé par ce fournisseur de magasins de messages.

 _lppMSProvider_
  
> [out] Pointeur vers un pointeur vers l’objet fournisseur de magasin de messages initialisé.

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.

MAPI_E_VERSION
  
> La version SPI utilisée par MAPI n’est pas compatible avec la spi utilisée par ce fournisseur.

## <a name="remarks"></a>Remarques

MAPI appelle la fonction de point d’entrée **MSProviderInit** pour initialiser un fournisseur de magasins de messages à la suite d’une ouverture de compte client.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Un fournisseur de magasins de messages doit implémenter **MSProviderInit** en tant que fonction de point d’entrée dans la DLL du fournisseur. L’implémentation doit être basée sur le prototype **de fonction MSPROVIDERINIT** , également spécifié dans MAPISPI.H. MAPI définit **MSPROVIDERINIT** pour utiliser le type d’appel d’initialisation MAPI standard, STDMAPIINITCALLTYPE, qui entraîne **MSProviderInit** à respecter la convention d’appel CDECL. Un avantage de CDECL est que les appels peuvent être tentés même si le nombre de paramètres d’appel ne correspond pas au nombre de paramètres définis.
  
Un fournisseur peut être initialisé plusieurs fois, suite à l’apparition de plusieurs profils dans une utilisation simultanée ou de l’apparition de plusieurs fois dans le même profil. Étant donné que l’objet fournisseur contient du contexte, **MSProviderInit** doit retourner un autre objet fournisseur dans _lppMSProvider_ pour chaque initialisation, même pour plusieurs initialisations dans le même processus.
  
La DLL du fournisseur ne doit pas être liée à Mapix.dll. Au lieu de cela, il doit utiliser ces pointeurs pour l’allocation ou la déallocation de la mémoire.
  
Le fournisseur de magasin de messages doit utiliser les fonctions pointées par  _lpAllocateBuffer_, _lpAllocateMore_ et _lpFreeBuffer_ pour la plupart des allocations et des déallocations de mémoire. En particulier, le fournisseur doit utiliser ces fonctions pour allouer de la mémoire aux applications clientes lors de l’appel d’interfaces d’objets telles que [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPITable::QueryRows](imapitable-queryrows.md). Si le fournisseur s’attend également à utiliser l’allocation de mémoire OLE, il doit appeler la méthode **IUnknown::AddRef** de l’objet allocateur pointé par le paramètre _lpMalloc_ .
  
Pour plus d’informations sur **l’écriture de MSProviderInit**, voir [Loading Message Store Providers](loading-message-store-providers.md). Pour plus d’informations sur les fonctions de point d’entrée, voir [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).
  
## <a name="see-also"></a>Voir aussi

[ABProviderInit](abproviderinit.md)  
[IMSProvider : IUnknown](imsprovideriunknown.md)  
[XPProviderInit](xpproviderinit.md)
