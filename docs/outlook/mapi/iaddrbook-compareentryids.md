---
title: IAddrBookCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBookCompareEntryIDs
api_type:
- COM
ms.assetid: 7dabc1d3-5ea4-482f-91a9-9ef3009eddd2
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 807e592cf535ac060fd275075035ae8beb7d6e78
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783607"
---
# <a name="iaddrbookcompareentryids"></a>IAddrBook::CompareEntryIDs

  
  
**S’applique à**: Outlook 
  
Compare deux identificateurs d’entrée qui appartiennent à un fournisseur de carnet d’adresse spécifique afin de déterminer si elles font référence à l’objet de carnet d’adresses même. 
  
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
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID1_ . 
    
 _lpEntryID1_
  
> [in] Pointeur vers le premier identificateur d’entrée à comparer.
    
 _cbEntryID2_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID2_ . 
    
 _lpEntryID2_
  
> [in] Pointeur vers le deuxième identificateur d’entrée à comparer.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpulResult_
  
> [out] Pointeur vers le résultat de la comparaison. Le contenu de _lpulResult_ est défini à TRUE si les identificateurs de deux entrée font référence au même objet ; Sinon, le contenu est défini sur FALSE. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Une ou les deux les identificateurs d’entrée passés avec les paramètres _lpEntryID1_ ou _lpEntryID2_ ne sont pas reconnus par n’importe quel fournisseur de carnet d’adresses. 
    
## <a name="remarks"></a>Remarques

Applications clientes et fournisseurs appel au service la méthode **CompareEntryIDs** pour comparer deux identificateurs d’entrée qui appartient à un fournisseur de carnet d’adresses unique pour déterminer si elles font référence au même objet. **CompareEntryIDs** est utile car un objet peut avoir plusieurs identificateurs d’entrée valide. Cette situation peut se produire, par exemple, après avoir installé une nouvelle version d’un fournisseur de carnet d’adresses. 
  
MAPI passe cet appel vers le fournisseur de carnet d’adresses qui est chargé des identificateurs d’entrée, en déterminant le fournisseur approprié en faisant correspondre la structure [MAPIUID](mapiuid.md) dans les identificateurs d’entrée avec la structure **MAPIUID** enregistrée par le fournisseur de services. 
  
Si les identificateurs de deux entrée font référence au même objet, **CompareEntryIDs** définit le contenu du paramètre _lpulResult_ sur TRUE ; s’ils font référence à des objets différents, **CompareEntryIDs** définit la valeur sur FALSE. Dans les deux cas, **CompareEntryIDs** renvoie S_OK. Si **CompareEntryIDs** renvoie une erreur qui peut se produire si aucun fournisseur de carnet d’adresses n’a inscrit une structure **MAPIUID** qui correspond à celui dans les identificateurs d’entrée, fournisseurs et clients ne doivent pas aucune action en fonction des résultats de la comparaison. Au lieu de cela, ils adopter l’approche la plus traditionnelle à l’action en cours d’exécution. 
  
## <a name="see-also"></a>Voir aussi



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

