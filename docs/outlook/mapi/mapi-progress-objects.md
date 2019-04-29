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
  
Les méthodes et les données d'un objet Progress vous permettent de contrôler l'état d'avancement de l'indicateur. Bien qu'un client ou MAPI implémente l'objet Progress, il est essentiel de s'assurer que l'affichage de la progression incombe aux fournisseurs de services. Vous pouvez garantir sa précision en spécifiant une ordre et une valeur spécifiques pour les paramètres transmis aux méthodes de l'objet Progress.
  
Les paramètres suivants sont transmis aux objets Progress:
  
- Masque de masque des indicateurs, défini avec [méthode imapiprogress:: SetLimits](imapiprogress-setlimits.md) et récupérés avec [méthode imapiprogress:: GetFlags](imapiprogress-getflags.md).
    
- Valeur minimale (locale et globale), définie avec **SetLimits** et récupérée avec [méthode imapiprogress:: GetMin](imapiprogress-getmin.md).
    
- Valeur maximale (locale et globale), définie avec **SetLimits** et récupérée avec [méthode imapiprogress:: GetMax](imapiprogress-getmax.md).
    
- Valeur qui indique le pourcentage d'achèvement actuel de l'opération, passé à [méthode imapiprogress::P rogress](imapiprogress-progress.md).
    
- Décompte du nombre d'objets qui ont été traités jusqu'à présent, passés à la **progression**.
    
- Nombre total d'objets impliqués dans l'opération, passés à la **progression**.
    
Tous les fournisseurs de services commencent leur traitement d'affichage de la progression avec un appel à **méthode imapiprogress: GetFlags** pour récupérer le paramètre présent Flags. Actuellement, les indicateurs peuvent être définis uniquement sur MAPI_TOP_LEVEL. Les clients et MAPI initialisent l'indicateur sur MAPI_TOP_LEVEL, en s'appuyant sur les fournisseurs de services pour les effacer, le cas échéant. 
  
La valeur flags est définie sur MAPI_TOP_LEVEL lorsque vous utilisez l'objet de niveau supérieur dans l'opération. L'objet de niveau supérieur est l'objet qui est appelé par le client pour commencer une opération. Dans une opération de copie de dossier, il s'agit du dossier copié. Dans une opération de suppression de dossier, il s'agit du dossier en cours de suppression. Lorsque vous effectuez un appel pour traiter un objet de niveau inférieur ou un sous-objet, effacez la valeur flags. Dans une opération de copie de dossier, les sous-objets sont les sous-dossiers qui se trouvent dans le dossier en cours de copie. 
  
MAPI vous permet de différencier les objets de niveau supérieur et les sous-objets à l'aide de l'indicateur MAPI_TOP_LEVEL afin que tous les objets impliqués dans une opération puissent utiliser la même implémentation [méthode imapiprogress](imapiprogressiunknown.md) pour afficher la progression, ce qui entraîne l'affichage de l'indicateur se déroule sans problème dans une seule direction positive. Que l'indicateur MAPI_TOP_LEVEL soit défini ou non affecte les paramètres des autres paramètres dans les appels ultérieurs à l'objet Progress. 
  
Étant donné qu'il est impossible de définir des valeurs de paramètre appropriées pour un affichage de la progression à tous les niveaux d'une opération multi-niveau, certains fournisseurs de services choisissent de ne pas afficher la progression des sous-objets. 
  
 **Pour éviter d'afficher la progression des sous-objets**
  
- Transmettre NULL pour le paramètre _lpProgress_ dans l'appel pour traiter un sous-objet. Par exemple, si vous copiez des dossiers, il s'agit de l'appel à la méthode [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md) d'un sous-dossier. 
    
- Écrire du code spécial pour déterminer comment interpréter le paramètre _lpProgress_ . Étant donné qu'une valeur NULL pour le paramètre _lpProgress_ peut également signifier que le client doit afficher la progression à l'aide de l'implémentation MAPI, un code spécial est nécessaire pour déterminer quand ignorer le paramètre _lpProgress_ et quand appeler [ IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md).
    
Appelez **méthode imapiprogress:: SetLimits** pour définir ou désélectionner l'indicateur MAPI_TOP_LEVEL et définir les valeurs minimales et maximales locales et globales. La valeur du paramètre flags détermine si l'objet Progress comprend les valeurs minimale et maximale qui doivent être locales ou globales. Lorsque l'indicateur MAPI_TOP_LEVEL est défini, ces valeurs sont considérées comme globales et sont utilisées pour calculer la progression de l'opération entière. Les objets Progress initialisent la valeur minimale globale à 0 et la valeur maximale globale à 1000. 
  
Lorsque MAPI_TOP_LEVEL n'est pas défini, les valeurs minimale et maximale sont considérées comme locales et sont utilisées en interne par les fournisseurs pour afficher la progression des sous-objets de niveau inférieur. Les objets Progress enregistrent uniquement les valeurs minimales et maximales de sorte qu'ils puissent être renvoyés aux fournisseurs lors de l'appel de **GetMin** et **GetMax** . 
  
La valeur, le nombre d'objets et le nombre total d'objets paramètres sont entrés dans la méthode **méthode imapiprogress::P rogress** . Le paramètre value, un nombre qui indique le pourcentage de progression, est obligatoire. Si l'indicateur MAPI_TOP_LEVEL est défini, vous pouvez également transmettre un nombre d'objets et un total d'objets. Certains clients utilisent ces valeurs pour afficher une phrase telle que «5 éléments terminés sur 10» avec l'indicateur de progression. La progression d'une opération peut être déclarée strictement sous forme de pourcentage ou de pourcentage et en termes de nombre d'éléments qui ont été traités du total à traiter. Par exemple, si vous êtes un fournisseur de banque de messages et que vous effectuez une opération de copie qui copie 10 dossiers, l'indicateur de progression peut fournir à l'utilisateur des informations supplémentaires en affichant une phrase telle que «1 sur 10», «2 de 10», «3 de 10». , et ainsi de suite jusqu'à la fin de l'opération. 
  
## <a name="see-also"></a>Voir aussi



[Indicateurs de progression MAPI](mapi-progress-indicators.md)

