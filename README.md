# Recursive
# Fonction recursive / JavaScript

const binarySearch = (array, thingToFind, start, end) => {
    
    if (start > end) {
        return false;
    }
    
    let mid = Math.floor((start + end) / 2);
    
    if (array[mid] === thingToFind) {
        return true;
    }
    
    if (thingToFind < array[mid]) {
        return binarySearch(array, thingToFind, start, mid - 1);
    } else {
        return binarySearch(array, thingToFind, mid + 1, end);
    }
}

Et voilà ! Une fonction récursive, qui s'appelle elle-même, qui effectue une recherche d'élément dans un tableau trié, et qui renvoie  true  si l'élément s'y trouve, ou  false  s'il ne s'y trouve pas (grâce au base case) !

Cet algorithme s'appelle la recherche binaire, et il s'agit d'un exercice qui est souvent demandé en entretien d'embauche, donc vous venez de faire un pas de plus vers votre premier emploi de développeur !
