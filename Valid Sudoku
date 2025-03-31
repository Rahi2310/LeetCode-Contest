class Solution {
public:
    bool isValidSudoku(vector<vector<char>>& board) {

        unordered_set<string> st;

        for(int i=0; i<9; i++)
        {
            for(int j=0; j<9; j++)
            {
                char c = board[i][j];

                if(c != '.')
                {
                    string row = string(1,c) + "_ROW_" + to_string(i);
                    string col = string(1,c) + "_COL_" + to_string(j);
                    string box = string(1,c) + "_box_" + to_string(i/3) + "_" + to_string(j/3);

                    if(st.find(row) != st.end() || st.find(col) != st.end() || st.find(box) != st.end())
                    return false;

                    st.insert(row);
                    st.insert(col);
                    st.insert(box);
                }
            }
        }

        return true;
        
    }
};
