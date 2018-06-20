---
title: Fonction Format (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 550fc235-f0b9-4d8e-805b-ce467821a8c9
description: Renvoie une valeur de mise en forme selon un modèle spécifié.
ms.openlocfilehash: 974b56ab8e6bc3f97c1931ba67ca9cd08c3511c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781845"
---
# <a name="format-function-access-custom-web-app"></a>Fonction Format (accès personnalisé web app)

Renvoie une valeur de mise en forme selon un modèle spécifié.
  
> [!NOTE]
> La fonctionnalité de stockage dans le nuage décrite dans cet article n’est plus pris en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > *Désolé, nous avons des problèmes de serveur, afin que nous ne pouvons pas ajouter \<service\> maintenant. Réessayez ultérieurement.* > Pour le stockage en nuage pour Office Online, Office pour iOS et Office pour Android, vous pouvez rechercher dans notre [Programme de partenariat de stockage dans le nuage Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

 **Format** (*Expression*, *Format*) 
  
La fonction **Format** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Expression*  <br/> |Expression d’un type de données pris en charge pour mettre en forme.  <br/> |
| *Format*  <br/> | Un modèle de format. L’argument format doit contenir une chaîne de format valide, sous la forme d’une chaîne de format standard (par exemple, « C » ou « D ») ou un modèle de caractères personnalisés pour les dates et les valeurs numériques (par exemple, « MMMM dd, yyyy (dddd) »). Pour plus d’informations, consultez la section Notes.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour le paramètre *Format* , vous pouvez passer des chaînes qui correspondent à un des modèles suivants : 
  
- [Chaînes de Format numérique standard](http://msdn.microsoft.com/en-us/library/dwhawy9k%28v=vs.110%29.aspx)
    
- [Chaînes de Format numérique personnalisé](http://msdn.microsoft.com/en-us/library/0c899ak8%28v=vs.110%29.aspx)
    
- [Chaînes de Format de Date et heure standard](http://msdn.microsoft.com/en-us/library/az4se3k1%28v=vs.110%29.aspx)
    
- [Chaînes de Format de Date et heure](http://msdn.microsoft.com/en-us/library/8kb3ddd4%28v=vs.110%29.aspx)
    
Vous ne pouvez pas utiliser la fonction **Format** dans les domaines suivants d’Access 2013 web applications : 
  
- Colonnes calculées au niveau de la table
    
- Macros de l’interface utilisateur
    
- Expressions dans les affichages (par exemple, dans les formulaires)
    

