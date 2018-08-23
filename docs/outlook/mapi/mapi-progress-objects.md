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
ms.openlocfilehash: c6079a62464231536c0fa6b5bacc291997fe38d9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567922"
---
# <a name="mapi-progress-objects"></a>Objets de progression MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Les méthodes et les données d’un objet de progression, vous pouvez contrôler comment l’indicateur signale la progression. Bien qu’un client ou un MAPI implémente l’objet de l’avancement, la plupart de la charge d’assurer l’exactitude de l’affichage de l’avancement se situe sur les fournisseurs de services. Vous pouvez garantir son exactitude en spécifiant une valeur pour les paramètres qui sont transmises aux méthodes d’objet de progression et un ordre particulier.
  
Les paramètres suivants sont transmis aux objets cours :
  
- Un masque de bits d’indicateurs, définie avec [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) et récupérés par [IMAPIProgress::GetFlags](imapiprogress-getflags.md).
    
- Valeur minimale (locale et globale), définie avec **SetLimits** et récupérés par [IMAPIProgress::GetMin](imapiprogress-getmin.md).
    
- Une valeur maximale (locale et globale), définie avec **SetLimits** et récupérés par [IMAPIProgress::GetMax](imapiprogress-getmax.md).
    
- Une valeur qui indique le pourcentage d’achèvement de l’opération, transmis à [IMAPIProgress::Progress](imapiprogress-progress.md).
    
- Le nombre d’objets qui ont été jusqu'à présent traités, transmises à la **progression**.
    
- Un nombre au nombre total d’objets impliqués dans l’opération, transmise à **l’avancement**.
    
Tous les fournisseurs de services commencent leur affichage en cours de traitement par un appel à **IMAPIProgress::GetFlags** pour récupérer les indicateurs présent définition. Actuellement, les indicateurs peuvent être définies qu’avec MAPI_TOP_LEVEL. Clients et MAPI initialiser l’indicateur MAPI_TOP_LEVEL, compter sur les fournisseurs de services pour la désactiver le cas échéant. 
  
La valeur flags est définie à MAPI_TOP_LEVEL lorsque vous travaillez avec l’objet de niveau supérieur dans l’opération. L’objet de niveau supérieur est l’objet qui est appelée par le client pour commencer une opération. Dans une opération de copie de dossier, c’est le dossier en cours de copie. Dans une opération de suppression de dossier, c’est le dossier en cours de suppression. Lorsque vous effectuez un appel à un objet de niveau inférieur de processus ou sous-objet, désactivez la valeur flags. Dans une opération de copie de dossier, sous-objets sont les sous-dossiers qui se trouvent dans le dossier en cours de copie. 
  
MAPI vous permet de faire la distinction entre les objets de niveau supérieur et sous-objets avec l’indicateur MAPI_TOP_LEVEL afin que tous les objets impliquant dans une opération peuvent utiliser la même implémentation [IMAPIProgress](imapiprogressiunknown.md) pour afficher la progression, ce qui provoque l’affichage de l’indicateur pour passez comme prévu dans un seul sens positif. Si l’indicateur MAPI_TOP_LEVEL est défini affecte les paramètres des autres paramètres dans les appels suivants à l’objet de progression. 
  
Car il peut être important de définir des valeurs de paramètre appropriée pour un affichage en cours à tous les niveaux d’une opération à plusieurs niveaux, certains fournisseurs de services de choisir de ne pas afficher la progression de sous-objets. 
  
 **Pour éviter d’afficher la progression de sous-objets**
  
- Passez la valeur NULL pour le paramètre _lpProgress_ dans l’appel à traiter un sous-objet. Par exemple, si vous copiez les dossiers, il s’agit de l’appel de méthode [d’IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) d’un sous-dossier. 
    
- Écrire du code spécial pour déterminer comment interpréter le paramètre _lpProgress_ . Une valeur NULL pour le paramètre _lpProgress_ peut également signifier que le client doit afficher l’avancement à l’aide de l’implémentation MAPI, code spécial est nécessaire afin de déterminer quand d’ignorer le paramètre _lpProgress_ et appelez [ IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md).
    
Appelez **IMAPIProgress::SetLimits** pour définir ou effacer l’indicateur MAPI_TOP_LEVEL et définir les valeurs minimales et maximales globales et locales. La valeur des indicateurs de la définition ou non affecte l’objet progression comprend les valeurs minimales et maximales pour être local ou global. Lorsque l’indicateur MAPI_TOP_LEVEL est défini, ces valeurs sont considérées comme globales et sont utilisés pour calculer l’avancement pour toute l’opération. Objets de progression initialiser la valeur minimale globale à 0 et la valeur maximale globale et 1000. 
  
Lorsque MAPI_TOP_LEVEL n’est pas définie, les valeurs minimales et maximales sont considérés comme étant locales et sont utilisés en interne par les fournisseurs pour afficher la progression de sous-objets de niveau inférieurs. Objets de progression enregistrement les valeurs minimales et maximales locales uniquement afin qu’ils peuvent être renvoyées à fournisseurs lorsque **GetMin** et **GetMax** sont appelées. 
  
La valeur, nombre d’objets et paramètres de l’objet total sont d’entrée à la méthode **IMAPIProgress::Progress** . Le paramètre value, un nombre qui indique le pourcentage d’avancement, est requis. Si l’indicateur MAPI_TOP_LEVEL est défini, vous pouvez également passer un nombre d’objets et un total de l’objet. Certains clients utilisent ces valeurs pour afficher une phrase tel que « 5 éléments terminé sur 10 » avec l’indicateur de progression. Progression d’une opération peut être signalée strictement sous forme de pourcentage ou sous forme de pourcentage et en termes de nombre d’éléments qui ont été traitées en dehors du total à traiter. Par exemple, si vous êtes un fournisseur de magasin de message et vous effectuez une opération de copie qui copie les 10 dossiers, l’indicateur de progression peut fournir des informations supplémentaires à l’utilisateur en affichant une phrase tel que « 1 de 10 », « 2 sur 10 », « 3 10 » , et ainsi de suite jusqu'à ce que l’opération est terminée. 
  
## <a name="see-also"></a>Voir aussi



[Indicateurs de progression MAPI](mapi-progress-indicators.md)

