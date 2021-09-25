---
title: IAddrBookCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBookCompareEntryIDs
api_type:
- COM
ms.assetid: 7dabc1d3-5ea4-482f-91a9-9ef3009eddd2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 773391c12d6100482d27c7bf023e4b75f56c195c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571856"
---
# <a name="iaddrbookcompareentryids"></a>IAddrBook::CompareEntryIDs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux identificateurs d’entrée appartenant à un fournisseur de carnet d’adresses particulier pour déterminer s’ils font référence au même objet de carnet d’adresses. 
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID1_
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID1._ 
    
 _lpEntryID1_
  
> [in] Pointeur vers le premier identificateur d’entrée à comparer.
    
 _cbEntryID2_
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID2._ 
    
 _lpEntryID2_
  
> [in] Pointeur vers le deuxième identificateur d’entrée à comparer.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpulResult_
  
> [out] Pointeur vers le résultat de la comparaison. Le contenu de  _lpulResult_ est définie sur TRUE si les deux identificateurs d’entrée font référence au même objet ; Dans le cas contraire, le contenu est définie sur FALSE. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L’un ou les deux identificateurs d’entrée transmis avec les paramètres  _lpEntryID1_ ou  _lpEntryID2_ ne sont reconnus par aucun fournisseur de carnet d’adresses. 
    
## <a name="remarks"></a>Remarques

Les applications clientes et les fournisseurs de services appellent la méthode **CompareEntryIDs** pour comparer deux identificateurs d’entrée appartenant à un seul fournisseur de carnet d’adresses afin de déterminer s’ils font référence au même objet. **CompareEntryIDs est utile** car un objet peut avoir plusieurs identificateurs d’entrée valides. Cette situation peut se produire, par exemple, après l’installation d’une nouvelle version d’un fournisseur de carnet d’adresses. 
  
MAPI transmet cet appel au fournisseur de carnet d’adresses responsable des identificateurs d’entrée, en déterminant le fournisseur approprié en faisant correspondre la structure [MAPIUID](mapiuid.md) dans les identificateurs d’entrée avec la structure **MAPIUID** inscrite par le fournisseur. 
  
Si les deux identificateurs d’entrée font référence au même objet, **CompareEntryIDs** définit le contenu du paramètre  _lpulResult_ sur TRUE ; S’ils font référence à différents objets, **CompareEntryIDs** définit le contenu sur FALSE. Dans les deux cas, **CompareEntryIDs** renvoie S_OK. Si **CompareEntryIDs** renvoie une erreur, qui peut se produire si aucun fournisseur de carnet d’adresses n’a inscrit une structure **MAPIUID** qui correspond à celle des identificateurs d’entrée, les clients et les fournisseurs ne doivent pas prendre d’action en fonction du résultat de la comparaison. Au lieu de cela, ils doivent prendre l’approche la plus prudent de l’action en cours. 
  
## <a name="see-also"></a>Voir aussi



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

