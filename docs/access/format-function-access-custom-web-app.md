---
title: Fonction de format (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: 550fc235-f0b9-4d8e-805b-ce467821a8c9
description: Renvoie une valeur mise en forme selon un modèle spécifié.
ms.localizationpriority: high
ms.openlocfilehash: eea5d5f20e746b22958b98e2e68953b52fbdf09a
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65893682"
---
# <a name="format-function-access-custom-web-app"></a>Fonction de format (application web personnalisée Access)

Renvoie une valeur mise en forme selon un modèle spécifié.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](/microsoft-365/cloud-storage-partner-program/)
  
## <a name="syntax"></a>Syntaxe

 **Format** (*Expression*, *Format*)
  
La fonction **Format** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Expression*  <br/> |Expression d’un type de données pris en charge à mettre en forme. |
| *Format*  <br/> | Modèle de format. L’argument de format doit contenir une chaîne de format valide, soit en tant que chaîne de format standard (par exemple, « C » ou « D ») soit en tant que modèle de caractères personnalisés pour les dates et les valeurs numériques (par exemple, « MMMM dd, aaaa (dddd) »). Pour plus d’informations, consultez Remarques. |

## <a name="remarks"></a>Remarques

Pour le paramètre *Format*, passez des chaînes qui correspondent à l’un des modèles suivants :
  
- [Chaînes de format numériques standard](https://msdn.microsoft.com/library/dwhawy9k%28v=vs.110%29.aspx)

- [Chaînes de format numériques personnalisées](https://msdn.microsoft.com/library/0c899ak8%28v=vs.110%29.aspx)

- [Chaînes de format de date et heure standard](https://msdn.microsoft.com/library/az4se3k1%28v=vs.110%29.aspx)

- [Chaînes de format de date et heure personnalisées](https://msdn.microsoft.com/library/8kb3ddd4%28v=vs.110%29.aspx)

Vous ne pouvez pas utiliser la fonction **Format** dans les zones suivantes d’applications web Access 2013 :
  
- Colonnes calculées au niveau du tableau

- Macros d’interface utilisateur

- Expressions dans les vues (par exemple, dans les formulaires)
