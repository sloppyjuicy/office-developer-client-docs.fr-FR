---
title: IMAPIStatusSettingsDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.SettingsDialog
api_type:
- COM
ms.assetid: e931246e-7fff-4116-a9fc-f685988e21e8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1e9d390a895490f2f7445c5f1ed6e0bde3a87639
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439729"
---
# <a name="imapistatussettingsdialog"></a>IMAPIStatus::SettingsDialog

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Affiche une feuille de propriétés qui permet à l’utilisateur de modifier la configuration d’un fournisseur de services Cette méthode n’est pas prise en charge dans les objets d’état implémentés par MAPI.
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Poignée vers la fenêtre parente de la feuille des propriétés de configuration.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’affichage de la feuille des propriétés. L’indicateur suivant peut être définie :
    
UI_READONLY 
  
> Suggère que le fournisseur ne doit pas permettre aux utilisateurs de modifier les propriétés de configuration. Cet indicateur n’est qu’une suggestion . il peut être ignoré.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La feuille des propriétés de configuration a été affichée avec succès.
    
MAPI_E_NO_SUPPORT 
  
> L’objet status ne prend pas en charge cette méthode, comme indiqué par l’absence de l’indicateur STATUS_SETTINGS_DIALOG dans la propriété **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIStatus::SettingsDialog** affiche une feuille des propriétés de configuration. Tous les fournisseurs de services doivent prendre en charge **la méthode SettingsDialog,** mais elle n’est pas obligatoire. Les fournisseurs de services peuvent implémenter leurs propres feuilles de propriétés ou utiliser l’implémentation fournie dans la méthode [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) de l’objet de support. **DoConfigPropsheet** crée une feuille de propriétés en lecture/écriture. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si un fournisseur de transport distant possède des paramètres, il doit :
  
- Ouvrez la section de profil du fournisseur de transport.
    
- Obtenez les paramètres de propriété du fournisseur de transport à partir du profil.
    
- Afficher les paramètres de propriété dans une boîte de dialogue.
    
- Si la boîte de dialogue autorise la modification des paramètres de propriété, vérifiez que les nouveaux paramètres sont valides et stockez-les dans la section de profil du fournisseur de transport.
    
- Renvoyer S_OK ou toute valeur d’erreur renvoyée au cours des étapes précédentes.
    
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez utiliser la feuille des propriétés affichée via **SettingsDialog** pour effectuer diverses tâches, telles que les suivantes : 
  
- Spécifiez une magasin de messages par défaut.
    
- Spécifiez un ordre de transport.
    
- Spécifiez un conteneur de carnet d’adresses par défaut pour la navigation.
    
- Spécifiez un ordre de recherche pour la résolution des noms ambigus.
    
- Spécifiez un carnet d’adresses personnel par défaut.
    
Les fournisseurs de services peuvent implémenter des feuilles de propriétés qui sont en lecture/écriture, en lecture seule ou une combinaison d’autorisations, selon la propriété. Les fournisseurs de services peuvent implémenter différentes autorisations sur des propriétés individuelles en fixant des restrictions de propriété. Le mode par défaut pour les feuilles de propriétés est en lecture-écriture. Vous pouvez demander des feuilles de propriétés en lecture seule en UI_READONLY’indicateur dans vos appels **à SettingsDialog**. Les fournisseurs de services qui sont en mesure d’implémenter des feuilles de propriétés en lecture seule peuvent le faire. Toutefois, étant donné que certains fournisseurs de services ne peuvent pas remplacer le mode par défaut, vous devez être prêt à gérer les feuilles de propriétés de l’un ou l’autre type. 
  
Étant donné qu’une interface utilisateur est toujours impliquée dans cette opération, seuls les clients interactifs doivent appeler **SettingsDialog**.
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)
  
[Propriété canonique PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

