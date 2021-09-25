---
title: IMAPISupportModifyStatusRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.ModifyStatusRow
api_type:
- COM
ms.assetid: a304ca8f-e404-4535-be76-0b673f2061a0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 19292d41e04b4a80d69ce68a1961c1deacbfde71
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625426"
---
# <a name="imapisupportmodifystatusrow"></a>IMAPISupport::ModifyStatusRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Modifie le tableau d’état en ajoutant une nouvelle ligne ou en modifiant une ligne existante.
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _cValues_
  
> [in] Nombre de propriétés à inclure dans la ligne du tableau d’état nouveau ou modifié. 
    
 _lpColumnVals_
  
> [in] Pointeur vers un tableau de valeurs de propriété qui décrivent les propriétés à inclure en tant que colonnes dans la ligne du tableau d’état nouveau ou modifié.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le traitement des informations qui définissent la ligne de tableau d’état. L’indicateur suivant peut être définie :
    
STATUSROW_UPDATE 
  
> Indique à MAPI de fusionner les propriétés incluses dans le tableau pointé par  _lpColumnVals_ avec une ligne de tableau d’état existante, plutôt que dans une nouvelle ligne. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table d’état a été correctement mise à jour.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::ModifyStatusRow** est implémentée pour tous les objets de prise en charge du fournisseur de services. Les fournisseurs de services **appellent ModifyStatusRow** au moment de l’ouverture de session pour ajouter une ligne à la table d’état et à d’autres moments de la session pour mettre à jour la ligne. **ModifyStatusRow fournit** à MAPI les informations nécessaires pour créer la table d’état. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Définissez l STATUSROW_UPDATE lorsque vous appelez **ModifyStatusRow** pour apporter des modifications aux propriétés de la ligne de votre table d’état existante. Cela informe MAPI que seules les colonnes modifiées sont passées dans le _paramètre lpColumnVals._ 
  
Les clients peuvent utiliser les informations de la table d’état pour accéder à votre objet d’état. 
  
Pour obtenir la liste complète des colonnes que vous devez inclure dans la ligne de votre tableau d’état, voir [Tableaux d’état.](status-tables.md)
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport : IUnknown](imapisupportiunknown.md)

