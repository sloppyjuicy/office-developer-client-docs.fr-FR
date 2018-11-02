---
title: IMAPISupportModifyStatusRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyStatusRow
api_type:
- COM
ms.assetid: a304ca8f-e404-4535-be76-0b673f2061a0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 06a5c9de5c0ce4c0f936791086a731a55510a124
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592142"
---
# <a name="imapisupportmodifystatusrow"></a>IMAPISupport::ModifyStatusRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Modifie la table d’état en ajoutant une nouvelle ligne ou de modification d’une ligne existante.
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _cValues_
  
> [in] Le nombre de propriétés à inclure dans la ligne de tableau état créé ou modifié. 
    
 _lpColumnVals_
  
> [in] Pointeur vers un tableau de valeurs de propriété qui décrivent les propriétés à inclure en tant que colonnes dans la ligne de tableau état créé ou modifié.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le mode de traitement des informations qui définissent la ligne table d’état. Vous pouvez définir l’indicateur suivant :
    
STATUSROW_UPDATE 
  
> Indique à MAPI pour fusionner les propriétés incluses dans le tableau vers lequel pointe _lpColumnVals_ avec une ligne de tableau d’état existante, plutôt que dans une nouvelle ligne. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La table d’état a été correctement mis à jour.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::ModifyStatusRow** est implémentée pour tous les objets de prise en charge de fournisseur de service. Fournisseurs de services d’appel **ModifyStatusRow** au moment de l’ouverture de session pour ajouter une ligne à la table d’état et à d’autres moments pendant la session de mise à jour de la ligne. **ModifyStatusRow** MAPI fournit les informations nécessaires pour créer la table d’état. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Définir l’indicateur STATUSROW_UPDATE lorsque vous appelez **ModifyStatusRow** pour modifier les propriétés dans la ligne de tableau état existant. Cela informe MAPI que seules les colonnes modifiées sont passés dans le paramètre _lpColumnVals_ . 
  
Clients peuvent utiliser les informations dans la table d’état pour accéder à votre objet d’état. 
  
Pour obtenir une liste complète des colonnes que vous devez inclure dans votre ligne de tableau d’état, voir les [Tableaux d’état](status-tables.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport : IUnknown](imapisupportiunknown.md)

