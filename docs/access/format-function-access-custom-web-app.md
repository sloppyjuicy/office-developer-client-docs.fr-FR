---
title: Fonction de format (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: 550fc235-f0b9-4d8e-805b-ce467821a8c9
description: Renvoie une valeur mise en forme selon un modèle spécifié.
localization_priority: Priority
ms.openlocfilehash: 5331df30f276a7edd0571e9bf24c759d57ec6a54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308203"
---
# <a name="format-function-access-custom-web-app"></a>Fonction de format (application web personnalisée Access)

Renvoie une valeur mise en forme selon un modèle spécifié.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. ») > En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage). 
  
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
    

