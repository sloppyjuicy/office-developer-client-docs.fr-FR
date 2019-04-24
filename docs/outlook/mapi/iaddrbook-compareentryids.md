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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: b6abecc298df7a86afff9338752a15615c73b3a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348887"
---
# <a name="iaddrbookcompareentryids"></a>IAddrBook::CompareEntryIDs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux identificateurs d'entrée qui appartiennent à un fournisseur de carnets d'adresses particulier pour déterminer s'ils font référence au même objet de carnet d'adresses. 
  
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
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID1_ . 
    
 _lpEntryID1_
  
> dans Pointeur vers le premier identificateur d'entrée à comparer.
    
 _cbEntryID2_
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID2_ . 
    
 _lpEntryID2_
  
> dans Pointeur vers le deuxième identificateur d'entrée à comparer.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpulResult_
  
> remarquer Pointeur vers le résultat de la comparaison. Le contenu de _lpulResult_ est défini sur true si les deux identificateurs d'entrée font référence au même objet; dans le cas contraire, le contenu est défini sur FALSe. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Un ou les deux identificateurs d'entrée passés avec les paramètres _lpEntryID1_ ou _lpEntryID2_ ne sont pas reconnus par les fournisseurs de carnets d'adresses. 
    
## <a name="remarks"></a>Remarques

Les applications clientes et les fournisseurs de services appellent la méthode **CompareEntryIDs** pour comparer deux identificateurs d'entrée appartenant à un fournisseur de carnets d'adresses unique afin de déterminer s'ils font référence au même objet. **CompareEntryIDs** est utile, car un objet peut avoir plus d'un identificateur d'entrée valide. Cette situation peut se produire, par exemple, après l'installation d'une nouvelle version d'un fournisseur de carnet d'adresses. 
  
MAPI transmet cet appel au fournisseur de carnets d'adresses qui est responsable des identificateurs d'entrée, en déterminant le fournisseur approprié en faisant correspondre la structure [MAPIUID](mapiuid.md) dans les identificateurs d'entrée à la structure **MAPIUID** inscrite par le moteur. 
  
Si les deux identificateurs d'entrée font référence au même objet, **CompareEntryIDs** définit le contenu du paramètre _lpulResult_ sur true; s'ils font référence à des objets différents, **CompareEntryIDs** définit le contenu sur false. Dans les deux cas, **CompareEntryIDs** renvoie S_OK. Si **CompareEntryIDs** renvoie une erreur, ce qui peut se produire si aucun fournisseur de carnet d'adresses n'a inscrit une structure **MAPIUID** qui correspond à celle des identificateurs d'entrée, les clients et les fournisseurs ne doivent effectuer aucune action en fonction du résultat de la COMP. Elles doivent plutôt adopter l'approche la plus conservatrice de l'action en cours d'exécution. 
  
## <a name="see-also"></a>Voir aussi



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

