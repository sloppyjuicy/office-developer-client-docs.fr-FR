---
title: ABProviderInit
description: ABProviderInit initialise un fournisseur de carnet d’adresses pour l’opération. Cet article décrit sa syntaxe, ses paramètres, sa valeur de retour et ses remarques.
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
ms.openlocfilehash: 4b7d8b48564d6beebe00c59fbbae388b4a0334c6
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770011"
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
  
> [in] Instance de la bibliothèque de liens dynamiques (DLL) du fournisseur de carnet d’adresses utilisée par MAPI lorsqu’elle est liée.

 _lpMalloc_
  
> [in] Pointeur vers un objet allocateur de mémoire exposant l’interface OLE **IMalloc** . Le fournisseur de carnet d’adresses peut avoir besoin d’utiliser cette méthode d’allocation lors de l’utilisation de certaines interfaces telles que **IStream**.

 _lpAllocateBuffer_
  
> [in] Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser lorsque MAPI l’exige pour allouer de la mémoire.

 _lpAllocateMore_
  
> [in] Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) , à utiliser lorsque MAPI l’exige pour allouer de la mémoire supplémentaire.

 _lpFreeBuffer_
  
> [in] Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) , à utiliser lorsque MAPI l’exige pour libérer de la mémoire.

 _ulFlags_
  
> [in] Masque de bits des indicateurs. L’indicateur suivant peut être défini :

MAPI_NT_SERVICE
  
> Le fournisseur est chargé dans le contexte d’un service Windows, un type spécial de processus sans accès à une interface utilisateur.

 _ulMAPIVer_
  
> [in] Numéro de version de l’interface du fournisseur de services (SPI) que MAPI.DLL utilise. Pour le numéro de version actuel, consultez mapISPI. Fichier d’en-tête H.

 _lpulProviderVer_
  
> [out] Pointeur vers le numéro de version du SPI utilisé par ce fournisseur de carnet d’adresses.

 _lppABProvider_
  
> [out] Pointeur vers un pointeur vers l’objet fournisseur de carnet d’adresses initialisé.

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.

MAPI_E_VERSION
  
> La version SPI utilisée par MAPI n’est pas compatible avec le SPI utilisé par ce fournisseur.

## <a name="remarks"></a>Remarques

MAPI appelle la fonction de point d’entrée **ABProviderInit** pour initialiser un fournisseur de carnet d’adresses à la suite d’une ouverture de session du client.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Un fournisseur de carnet d’adresses doit **implémenter ABProviderInit** en tant que fonction de point d’entrée dans la DLL du fournisseur. L’implémentation doit être basée sur le prototype de fonction **ABPROVIDERINIT** , également spécifié dans MAPISPI.H. MAPI définit **ABPROVIDERINIT** pour utiliser le type d’appel d’initialisation MAPI standard, STDMAPIINITCALLTYPE, ce qui amène **ABProviderInit** à suivre la convention d’appel CDECL.
  
Un fournisseur peut être initialisé plusieurs fois, en raison de l’affichage simultané de plusieurs profils dans plusieurs profils ou de l’affichage plusieurs fois dans le même profil. Étant donné que l’objet fournisseur contient du contexte, **ABProviderInit** doit retourner un objet fournisseur différent dans _lppABProvider_ pour chaque initialisation, même pour plusieurs initialisations dans le même processus.
  
Le fournisseur de carnet d’adresses doit utiliser les fonctions pointées par _lpAllocateBuffer_, _lpAllocateMore_ et _lpFreeBuffer_ pour la plupart de l’allocation et de la désallocation de la mémoire. En particulier, le fournisseur doit utiliser ces fonctions pour allouer de la mémoire à utiliser par les applications clientes lors de l’appel d’interfaces d’objet telles que [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPITable::QueryRows](imapitable-queryrows.md). Si le fournisseur s’attend également à utiliser l’allocateur de mémoire OLE, il doit appeler la méthode **IUnknown::AddRef** de l’objet allocateur pointé par le paramètre _lpMalloc_ .
  
Pour plus d’informations sur l’écriture **d’ABProviderInit**, consultez [Implémentation d’une fonction de point d’entrée du fournisseur de carnet d’adresses](implementing-an-address-book-provider-entry-point-function.md). Pour plus d’informations sur les fonctions de point d’entrée, consultez [Implémentation d’une fonction de point d’entrée du fournisseur de services](implementing-a-service-provider-entry-point-function.md).
  
## <a name="see-also"></a>Voir aussi

- [IABProvider : IUnknown](iabprovideriunknown.md)
- [MSProviderInit](msproviderinit.md)
- [XPProviderInit](xpproviderinit.md)
