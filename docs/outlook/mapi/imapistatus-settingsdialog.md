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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 09a14a3cc9f77527c6bc254dc703328f2c9ce9f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783964"
---
# <a name="imapistatussettingsdialog"></a>IMAPIStatus::SettingsDialog

  
  
**S’applique à**: Outlook 
  
Affiche une feuille de propriétés qui permet à l’utilisateur de modifier la configuration d’un fournisseur de services que cette méthode n’est pas pris en charge dans les objets état implémentés par MAPI.
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Un handle vers la fenêtre parent de la feuille de propriétés de configuration.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’affichage de la feuille de propriétés. Vous pouvez définir l’indicateur suivant :
    
UI_READONLY 
  
> Indique que le fournisseur ne doit pas activer aux utilisateurs de modifier les propriétés de configuration. Cet indicateur n’est qu’une suggestion ; Il peut être ignoré.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La feuille de propriétés de configuration a été correctement affichée.
    
MAPI_E_NO_SUPPORT 
  
> L’objet état ne gère pas cette méthode, comme indiqué par l’absence de l’indicateur STATUS_SETTINGS_DIALOG dans la propriété **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIStatus::SettingsDialog** affiche une feuille de propriétés de configuration. Tous les fournisseurs de services doivent prendre en charge la méthode **dialogue** , mais il n’est pas nécessaire. Fournisseurs de service peuvent implémenter leurs propres feuilles de propriétés ou utilisez l’implémentation fournie dans la méthode [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) de l’objet de la prise en charge. **DoConfigPropsheet** génère une feuille de propriétés en lecture-écriture. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Si un fournisseur de transport à distance possède des paramètres, il doit procédez comme suit :
  
- Ouvrez la section de profil du fournisseur de transport.
    
- Obtenez le transport paramètres du fournisseur de la propriété du profil.
    
- Afficher les paramètres des propriétés dans une boîte de dialogue.
    
- Si la boîte de dialogue permet de modifier les paramètres de la propriété, vérifiez que les nouveaux paramètres sont valides et les stockent dans la section de profil du fournisseur de transport.
    
- Renvoie S_OK, ou les valeurs d’erreur renvoyés au cours des étapes précédentes.
    
## <a name="notes-to-callers"></a>Notes aux appelants

Vous pouvez utiliser la feuille des propriétés affichée par le biais de **dialogue** pour effectuer diverses tâches, telles que les suivantes : 
  
- Spécifiez une banque de messages par défaut.
    
- Spécifier un ordre de transport.
    
- Spécifier un conteneur de carnet d’adresses par défaut pour la navigation.
    
- Spécifiez un ordre de recherche pour la résolution des noms ambigus.
    
- Spécifiez un carnet d’adresses personnel par défaut.
    
Fournisseurs de services peuvent implémenter des feuilles de propriétés qui sont en lecture/écriture, en lecture seule, ou une combinaison des autorisations en fonction de la propriété. Fournisseurs de services peuvent implémenter des autorisations différentes sur des propriétés individuelles en définissant les restrictions de propriété. Le mode par défaut pour les feuilles de propriété est en lecture-écriture. Vous pouvez demander des feuilles de propriétés en lecture seule en définissant l’indicateur UI_READONLY dans vos appels à **dialogue**. Fournisseurs de services qui sont en mesure d’implémenter des feuilles de propriétés en lecture seule peuvent le faire. Étant donné que certains fournisseurs de services ne peuvent pas modifier le mode par défaut, vous devez être prêt à gérer les feuilles de propriétés de des types. 
  
Car une interface utilisateur est toujours impliquée dans cette opération, seuls les clients interactives doivent appeler **dialogue**.
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)
  
[Propriété canonique PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

