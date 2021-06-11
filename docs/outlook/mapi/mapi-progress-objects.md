---
title: Objets de progression MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e446004e-1ef2-4e58-b764-de7b4dcefaf1
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 73d905028f8f62ad8cbb9da9b1ad61b8cab1065e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422025"
---
# <a name="mapi-progress-objects"></a>Objets de progression MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avec les méthodes et les données d’un objet de progression, vous pouvez contrôler la façon dont l’indicateur signale la progression. Bien qu’un client ou MAPI implémente l’objet de progression, la plus grande partie de la tâche de garantir l’correctité de l’affichage de l’avancement incombe aux fournisseurs de services. Vous pouvez garantir sa précision en spécifiant un ordre et une valeur particuliers pour les paramètres transmis aux méthodes d’objet de progression.
  
Les paramètres suivants sont transmis aux objets de progression :
  
- Masque de bits d’indicateurs, définie avec [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) et récupérée avec [IMAPIProgress::GetFlags](imapiprogress-getflags.md).
    
- Valeur minimale (locale et globale), définie avec **SetLimits** et récupérée avec [IMAPIProgress::GetMin](imapiprogress-getmin.md).
    
- Valeur maximale (locale et globale), définie avec **SetLimits** et récupérée avec [IMAPIProgress::GetMax](imapiprogress-getmax.md).
    
- Valeur qui indique le pourcentage actuel d’achèvement de l’opération, transmise à [IMAPIProgress::P rogress](imapiprogress-progress.md).
    
- Nombre d’objets qui ont été jusqu’ici traitées, transmis à **Progress**.
    
- Nombre total d’objets impliqués dans l’opération, transmis à **Progress**.
    
Tous les fournisseurs de services commencent leur traitement d’affichage de progression par un appel à **IMAPIProgress::GetFlags** pour récupérer le paramètre des indicateurs présents. Actuellement, les indicateurs peuvent être uniquement MAPI_TOP_LEVEL. Les clients et MAPI initialisent l’indicateur MAPI_TOP_LEVEL, en s’appuyant sur les fournisseurs de services pour l’effacer le cas échéant. 
  
La valeur des indicateurs est définie sur MAPI_TOP_LEVEL lorsque vous travaillez avec l’objet de niveau supérieur dans l’opération. L’objet de niveau supérieur est l’objet qui est appelé par le client pour commencer une opération. Dans une opération de copie de dossier, il s’agit du dossier en cours de copie. Dans une opération de suppression de dossier, il s’agit du dossier en cours de suppression. Lorsque vous appelez pour traiter un objet de niveau inférieur, ou sous-objet, effacer la valeur des indicateurs. Dans une opération de copie de dossier, les sous-dossiers sont les sous-dossiers du dossier en cours de copie. 
  
MAPI vous permet de différencier les objets de niveau supérieur des sous-objets avec l’indicateur MAPI_TOP_LEVEL afin que tous les objets impliqués dans une opération peuvent utiliser la même implémentation [IMAPIProgress](imapiprogressiunknown.md) pour afficher la progression, ce qui a pour effet que l’affichage de l’indicateur se déroule sans problèmes dans une seule direction positive. Si l’indicateur MAPI_TOP_LEVEL est ou non définie affecte les paramètres des autres paramètres dans les appels ultérieurs à l’objet de progression. 
  
Comme il peut être impossible de définir des valeurs de paramètre appropriées pour un affichage de progression à tous les niveaux d’une opération à plusieurs niveaux, certains fournisseurs de services choisit de ne pas afficher la progression des sous-objets. 
  
 **Pour éviter d’afficher la progression des sous-objets**
  
- Passez NULL pour le  _paramètre lpProgress_ dans l’appel pour traiter un sous-objet. Par exemple, si vous copiez des dossiers, il s’agit de l’appel à la méthode [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) d’un sous-dossier. 
    
- Écrivez du code spécial pour déterminer comment interpréter _le paramètre lpProgress._ Étant donné qu’une valeur NULL pour le paramètre  _lpProgress_ peut également signifier que le client doit afficher la progression à l’aide de l’implémentation MAPI, un code spécial est nécessaire pour déterminer quand ignorer le paramètre  _lpProgress_ et quand appeler [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md).
    
Appelez **IMAPIProgress::SetLimits** pour définir ou effacer l’indicateur MAPI_TOP_LEVEL et pour définir les valeurs minimales et maximales locales et globales. La valeur du paramètre indicateurs a une incidence sur le fait que l’objet de progression comprenne les valeurs minimale et maximale à être locales ou globales. Lorsque l MAPI_TOP_LEVEL est définie, ces valeurs sont considérées comme globales et sont utilisées pour calculer la progression de l’ensemble de l’opération. Les objets de progression initialisent la valeur minimale globale sur 0 et la valeur maximale globale à 1 000. 
  
Lorsque MAPI_TOP_LEVEL n’est pas définie, les valeurs minimale et maximale sont considérées comme locales et sont utilisées en interne par les fournisseurs pour afficher la progression des sous-objets de niveau inférieur. Les objets de progression enregistrent les valeurs minimales et maximales locales uniquement afin de pouvoir être renvoyés aux fournisseurs lorsque **GetMin** et **GetMax** sont appelés. 
  
Les paramètres de valeur, de nombre d’objets et de nombre total d’objets sont entrées dans la méthode **IMAPIProgress::P rogress.** Le paramètre de valeur, un nombre qui indique le pourcentage de progression, est requis. Si l MAPI_TOP_LEVEL est définie, vous pouvez également transmettre un nombre d’objets et un total d’objets. Certains clients utilisent ces valeurs pour afficher une expression telle que « 5 éléments terminés sur 10 » avec l’indicateur de progression. L’avancement d’une opération peut être signalé strictement sous la mesure d’un pourcentage ou d’un pourcentage et en termes de nombre d’éléments qui ont été traitées sur le total à traiter. Par exemple, si vous êtes un fournisseur de magasins de messages et que vous effectuez une opération de copie qui copie 10 dossiers, l’indicateur de progression peut fournir à l’utilisateur des informations supplémentaires en affichant une expression telle que « 1 sur 10 », « 2 sur 10 », « 3 sur 10 », etc. jusqu’à ce que l’opération soit terminée. 
  
## <a name="see-also"></a>Voir aussi



[Indicateurs de progression MAPI](mapi-progress-indicators.md)

