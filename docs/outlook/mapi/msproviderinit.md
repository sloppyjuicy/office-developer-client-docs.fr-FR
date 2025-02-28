---
title: MSProviderInit
description: Décrit la syntaxe, les paramètres, la valeur de retour et les remarques pour MSProviderInit, qui initialise un fournisseur de magasin de messages pour l’opération.
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
ms.openlocfilehash: cecb9a6d7df366b3267bac1ea3926d9da036cea4
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828317"
---
# <a name="msproviderinit"></a>MSProviderInit

**S’applique à** : Outlook 2013 | Outlook 2016
  
Initialise un fournisseur de magasin de messages pour l’opération.
  
|Propriété|Valeur|
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
  
> [in] Instance de la bibliothèque de liens dynamiques (DLL) du fournisseur de magasin de messages utilisée par MAPI lors de son lien.

 _lpMalloc_
  
> [in] Pointeur vers un objet allocateur de mémoire exposant l’interface OLE **IMalloc** . Le fournisseur du magasin de messages peut avoir besoin d’utiliser cette méthode d’allocation lors de l’utilisation de certaines interfaces telles que **IStream**.

 _lpAllocateBuffer_
  
> [in] Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser pour allouer de la mémoire.

 _lpAllocateMore_
  
> [in] Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) , à utiliser pour allouer de la mémoire supplémentaire.

 _lpFreeBuffer_
  
> [in] Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) , à utiliser pour libérer de la mémoire.

 _ulFlags_
  
> [in] Masque de bits des indicateurs. L’indicateur suivant peut être défini :

MAPI_NT_SERVICE
  
> Le fournisseur est chargé dans le contexte d’un service Windows, un type spécial de processus sans accès à une interface utilisateur.

 _ulMAPIVer_
  
> [in] Numéro de version de l’interface de fournisseur de services (SPI) utilisée par MAPI. Pour le numéro de version actuel, consultez le fichier d’en-tête Mapispi.h.

 _lpulProviderVer_
  
> [out] Pointeur vers le numéro de version du SPI utilisé par ce fournisseur de magasin de messages.

 _lppMSProvider_
  
> [out] Pointeur vers un pointeur vers l’objet fournisseur du magasin de messages initialisé.

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.

MAPI_E_VERSION
  
> La version SPI utilisée par MAPI n’est pas compatible avec le SPI utilisé par ce fournisseur.

## <a name="remarks"></a>Remarques

MAPI appelle la fonction de point d’entrée **MSProviderInit** pour initialiser un fournisseur de magasin de messages à la suite d’une ouverture de session du client.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Un fournisseur de magasin de messages doit **implémenter MSProviderInit** en tant que fonction de point d’entrée dans la DLL du fournisseur. L’implémentation doit être basée sur le prototype de fonction **MSPROVIDERINIT** , également spécifié dans MAPISPI.H. MAPI définit **MSPROVIDERINIT** pour utiliser le type d’appel d’initialisation MAPI standard, STDMAPIINITCALLTYPE, ce qui amène **MSProviderInit** à suivre la convention d’appel CDECL. Un avantage de CDECL est que les appels peuvent être tentés même si le nombre de paramètres d’appel ne correspond pas au nombre de paramètres définis.
  
Un fournisseur peut être initialisé plusieurs fois, en raison de l’affichage simultané de plusieurs profils dans plusieurs profils ou de l’affichage plusieurs fois dans le même profil. Étant donné que l’objet fournisseur contient du contexte, **MSProviderInit** doit retourner un objet fournisseur différent dans _lppMSProvider_ pour chaque initialisation, même pour plusieurs initialisations dans le même processus.
  
La DLL du fournisseur ne doit pas être liée à Mapix.dll. Au lieu de cela, il doit utiliser ces pointeurs pour l’allocation ou la désallocation de la mémoire.
  
Le fournisseur du magasin de messages doit utiliser les fonctions pointées par  _lpAllocateBuffer_, _lpAllocateMore_ et _lpFreeBuffer_ pour la plupart de l’allocation et de la désallocation de la mémoire. En particulier, le fournisseur doit utiliser ces fonctions pour allouer de la mémoire à utiliser par les applications clientes lors de l’appel d’interfaces d’objet telles que [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPITable::QueryRows](imapitable-queryrows.md). Si le fournisseur s’attend également à utiliser l’allocateur de mémoire OLE, il doit appeler la méthode **IUnknown::AddRef** de l’objet allocateur pointé par le paramètre _lpMalloc_ .
  
Pour plus d’informations sur l’écriture de **MSProviderInit**, consultez [Loading Message Store Providers](loading-message-store-providers.md). Pour plus d’informations sur les fonctions de point d’entrée, consultez [Implémentation d’une fonction de point d’entrée du fournisseur de services](implementing-a-service-provider-entry-point-function.md).
  
## <a name="see-also"></a>Voir aussi

[ABProviderInit](abproviderinit.md)  
[IMSProvider : IUnknown](imsprovideriunknown.md)  
[XPProviderInit](xpproviderinit.md)
