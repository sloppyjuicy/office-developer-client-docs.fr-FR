---
title: Fonction de format (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: 550fc235-f0b9-4d8e-805b-ce467821a8c9
description: Renvoie une valeur mise en forme selon un modèle spécifié.
ms.localizationpriority: high
ms.openlocfilehash: cb7ec79c6d84027f7692fe51e1aa5ec74f2f5086
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62180305"
---
# <a name="format-function-access-custom-web-app"></a>Fonction de format (application web personnalisée Access)

Renvoie une valeur mise en forme selon un modèle spécifié.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](https://dev.office.com/programs/officecloudstorage)
  
## <a name="syntax"></a>Syntaxe

 **Format** (*Expression*, *Format*)
  
La fonction **Format** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Expression*  <br/> |Expression d’un type de données pris en charge à mettre en forme.  <br/> |
| *Format*  <br/> | Un modèle de format. L’argument Format doit contenir une chaîne de format valide, soit sous la forme d’une chaîne de format standard (par exemple, « C » ou « D ») ou d’un modèle de caractères personnalisés pour les dates et des valeurs numériques (par exemple, « MMMM jj, aaaa (jjjj) »). Pour plus d’informations, consultez la rubrique Remarques.  <br/> |

## <a name="remarks"></a>Remarques

Pour le paramètre *Format*, vous pouvez passer des chaînes qui correspondent à l’un des modèles suivants :
  
- [Chaînes de format numériques standard](https://msdn.microsoft.com/library/dwhawy9k%28v=vs.110%29.aspx)

- [Chaînes de format numériques personnalisées](https://msdn.microsoft.com/library/0c899ak8%28v=vs.110%29.aspx)

- [Chaînes de format de date et heure standard](https://msdn.microsoft.com/library/az4se3k1%28v=vs.110%29.aspx)

- [Chaînes de format de date et heure personnalisées](https://msdn.microsoft.com/library/8kb3ddd4%28v=vs.110%29.aspx)

Vous ne pouvez pas utiliser la fonction **Format** dans les zones suivantes d’applications web Access 2013 :
  
- Colonnes calculées au niveau du tableau

- Macros d’interface utilisateur

- Expressions dans les vues (par exemple, dans les formulaires)
